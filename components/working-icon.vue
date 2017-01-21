<template>
	<icon v-bind:i="currentIcon" 
		v-bind:class="(this.state === 'cog') ? 'spinning' : ''"/>
</template>

<script>
import Icon from '~components/icon.vue';

const WAITING  = 0,
      WORKING  = 'cog',
      SUCCEDED = 'check',
      FAILED   = 'times',
      TIMEOUT  = 1500;

export default {
	data: () => ({
		state: WAITING
	}),

	components: {
		Icon
	},

	props: ['i'],

	computed: {
		currentIcon() {
			if (this.state === WAITING) return this.i;
			return this.state;
		}
	},

	methods: {
		working() {
			this.state = WORKING;
		},

		succeeded() {
			this.state = SUCCEDED;

			setTimeout(() => {
				this.state = WAITING;
			}, TIMEOUT);
		},

		failed() {
			this.state = FAILED;

			setTimeout(() => {
				this.state = WAITING;
			}, TIMEOUT);
		}
	}
}
</script>