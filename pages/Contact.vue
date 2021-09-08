<template>
	<div>
		<!--h1>{{ title }}</!--h1!-->
		<v-row justify="center" align="center">
			<v-col cols="12" sm="6">
				<Forms />
			</v-col>
			<v-col cols="12" sm="6">
				<Info />
			</v-col>
		</v-row>
		<v-row>
			<Map />
		</v-row>
	</div>
</template>

<script>
export default {
	data() {
		return {
			title: "Please contact us..",
		};
	},
};
</script>

<style></style>
