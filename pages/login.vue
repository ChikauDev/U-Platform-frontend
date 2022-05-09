<template>
    <div class="bg-gray-50 min-h-screen flex flex-col">
        <div class="container max-w-md mx-auto flex-1 flex flex-col mt-10 px-2">
            <div class="bg-white px-6 py-8 rounded shadow-xl text-black w-full">
                <h1 class="mb-8 text-3xl text-center">Login</h1>
                
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

                <button
                    type="submit"
                    class="w-full text-center py-3 rounded bg-green-700 text-white hover:bg-green-dark focus:outline-none my-1"
                >Login</button>

            </div>

            <div class="text-grey-dark mt-6">
                You don't have an account? 
                <nuxt-link class="no-underline border-b border-blue text-blue" to="/signup">
                    Sign up here
                </nuxt-link>
            </div>

        </div>
    </div>
</template>