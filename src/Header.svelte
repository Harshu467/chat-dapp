<script>
    import { username, user } from './user';
    
    function signout() {
      user.leave();
      username.set('');
    }
  </script>

<header>
    <h1>FUN CHAT</h1>
    {#if $username}
    <div class="user-info">
        <span>Hello <strong>{$username}</strong></span>
        <img src={`https://avatars.dicebear.com/api/initials/${$username}.svg`} alt="avatar" />
    </div>
    <button class="signout-button" on:click={signout}>Sign Out</button>
    {:else}
      <h3>FUN.js Chat</h3>
  {/if}
</header>