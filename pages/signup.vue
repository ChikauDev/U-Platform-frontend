<template>
    <div class="bg-gray-50 min-h-screen flex flex-col">
        <div class="container max-w-md mx-auto flex-1 flex flex-col mt-10 px-2">
            <div class="bg-white px-6 py-8 rounded shadow-xl text-black w-full">
                <h1 class="mb-8 text-3xl text-center">Sign up</h1>
                
                <button
                    type="submit"
                    class="w-full text-center py-3 mb-10 rounded border-2 border-green-700 hover:bg-green-dark focus:outline-none my-1"
                >Google Account</button>

                <input 
                    type="text"
                    class="block border border-grey-light w-full p-3 rounded mb-4"
                    name="fullname"
                    placeholder="Full Name" />

                <input 
                    type="text"
                    class="block border border-grey-light w-full p-3 rounded mb-4"
                    name="email"
                    placeholder="Email" />

                <input 
                    type="password"
                    class="block border border-grey-light w-full p-3 rounded mb-4"
                    name="password"
                    placeholder="Password" />
                <input 
                    type="password"
                    class="block border border-grey-light w-full p-3 rounded mb-4"
                    name="confirm_password"
                    placeholder="Confirm Password" />

                <div class="mb-3">
                    <div class="form-check">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="checkbox" value="" id="flexCheckDefault">
                        <label class="form-check-label inline-block text-gray-800" for="flexCheckDefault">
                            I accept the <a href="/terms-of-use" class="text-indigo-700 underline">Terms of Use</a> & <a  class="text-indigo-700 underline" href="/privacy-policy">Privacy Policy</a>
                        </label>
                    </div>
                </div>  

                <button
                    type="submit"
                    class="w-full text-center py-3 rounded bg-green-700 text-white hover:bg-green-dark focus:outline-none my-1"
                >Create Account</button>

            </div>

            <div class="text-grey-dark mt-6">
                Already have an account? 
                <nuxt-link class="no-underline border-b border-blue text-blue underline" to='/login'
                >
                    Log in here
                </nuxt-link>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            form:{
                name: '',
                email: '',
                password: '',
                password_confirmation: '',
            }
        }
    },
    methods:{
        async submit(){
            try{
                await this.$axios.$post('register', this.form)
                await this.$auth.login({
                    data: {
                        email: this.form.email,
                        password: this.form.password,
                    }
                })

                // redirect
                this.$router.push({
                    path: this.$route.query.redirect || '/dashboard'
                })
            }
            catch(err){
                console.log(err)
            }
        }
    }
}
</script>