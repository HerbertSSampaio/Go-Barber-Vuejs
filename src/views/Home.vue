<template>
	<div class="home">
		<v-container class="pa-0" fluid>
			<v-row no-gutters>
				<v-col
					cols="12"
					sm="12"
					md="4"
				>
					<v-card class="pa-12 d-flex flex-column justify-space-around background-sign-in-color">
						<v-img
							src="../assets/logo.svg"
							max-height="150"
							max-width="250"
						/>
						<h1 class="font-weight-bold">
							Faça seu login
						</h1>
						<FormLogIn />
						<router-link class="text-decoration-none" to="/SignUp">
							<a class="orange--text">
								<v-icon class="orange--text">
									mdi-logout
								</v-icon>
								Criar conta
							</a>
						</router-link>
					</v-card>
				</v-col>
				<v-col
					cols="12"
					md="8"
				>
					<div class="background-sign-in-image" />
				</v-col>
			</v-row>
		</v-container>
	</div>
</template>

<script>
// @ is an alias to /src
	import FormLogIn from '@/components/FormLogIn.vue';

	export default {
		name: 'Home',
		components: {
			FormLogIn,
		},
	};
</script>

<style scoped>
	.background-sign-in-color {
		background-color: #312E38 !important;
		height: 100%;
		align-items: center;
	}

	.background-sign-in-image {
		background: url('../assets/sign-in-background.png');
		background-size: cover;
		height: 100vh;
	}
	.pa-0 {
		padding: 0 !important;
	}
</style>
