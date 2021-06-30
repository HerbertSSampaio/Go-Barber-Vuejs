<template>
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
		<v-btn
			:disabled="!valid"
			class="orange mb-4 px-16 py-6 black--text font-weight-bold"
			@click="validate"
		>
			Recuperar
		</v-btn>
	</v-form>
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
