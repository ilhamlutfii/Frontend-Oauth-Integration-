<script>
    import { GoogleLogin } from 'google-login-svelte'
 
    let user = null
 
    const handleSignin = (event) => {
       user = event.detail.profileObj
       console.log(`User ${user.name} signed in successfully`)
    }
 
    const handleFailure = (event) => {
       const err = event.detail
       console.error(`Error while signing in: `, err)
    }
 </script>
 
 <GoogleLogin 
    clientId="116260901621-5d7ojp12do5qkcl4peccsela565oq3ue.apps.googleusercontent.com"
    on:success={handleSignin}
    on:failure={handleFailure}
    let:signIn
 >
    <button on:click={signIn}>
       Sign in with Google
    </button>
 </GoogleLogin>
 
 {#if user}
    <h1>Welcome {user.name}</h1>
 {/if}