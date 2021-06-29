<template>
	<div class="SignUp">
		<v-container class="pa-0" fluid>
			<v-row no-gutters>
				<v-col
					cols="12"
					md="8"
				>
					<div class="background-sign-up-image" />
				</v-col>
				<v-col
					cols="12"
					sm="12"
					md="4"
				>
					<v-card class="pa-12 d-flex flex-column justify-space-around background-sign-up-color">
						<v-img
							src="../assets/logo.svg"
							max-height="150"
							max-width="250"
						/>
						<h1 class="font-weight-bold">
							Cadastre-se
						</h1>
						<FormSignUp />
						<a class="white--text">
							<v-icon class="white--text">
								mdi-arrow-left-bold
							</v-icon>
							Voltar para o login
						</a>
					</v-card>
				</v-col>
			</v-row>
		</v-container>
	</div>
</template>

<script>
// @ is an alias to /src
	import FormSignUp from '@/components/FormSignUp.vue';

	export default {
		name: 'SignUp',
		components: {
			FormSignUp,
		},
	};
</script>

<style scoped>
	.background-sign-up-color {
		background-color: #312E38 !important;
		height: 100%;
		align-items: center;
	}

	.background-sign-up-image {
		background: url('../assets/sign-up-background.png');
		background-size: cover;
		height: 100vh;
	}
	.pa-0 {
		padding: 0 !important;
	}
</style>
