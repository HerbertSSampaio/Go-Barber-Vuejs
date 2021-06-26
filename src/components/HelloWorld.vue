<template>
	<v-container>
		<v-row class="text-center justify-center align-center">
			<v-form
				ref="form"
				v-model="valid"
				lazy-validation
			>
				<v-text-field
					v-model="email"
					:rules="emailRules"
					label="E-mail"
					required
				/>
				<v-text-field
					v-model="password"
					label="Senha"
					:rules="passwordRules"
					type="password"
					required
				/>
				<v-btn
					:disabled="!valid"
					color="success"
					class="mr-4"
					@click="validate"
				>
					Entrar
				</v-btn>
			</v-form>
		</v-row>
	</v-container>
</template>
<script>
	export default {
		data: () => ({
			email: '',
			emailRules: [
				v => !!v || 'E-mail is required',
				v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
			],
			password: '',
			confirmPassword: '',
			passwordRules: [v => !!v || 'Password is required'],
		}),
		methods: {
			validate() {
				this.$refs.form.validate();
			},
		},
	};
</script>
