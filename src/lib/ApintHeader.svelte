
<svelte:options customElement="apint-header" />

<script>
  import ApintButton from "./ApintButton.svelte";

  const { title = "Apint.org", supportuser = false, user = undefined, icon = "" } = $props();
</script>

<header>
  <div class="header">
    <div>

      {#if icon}
        <img src={icon} width="32px" height="32px" alt="home" />
      {/if}

      <!-- <svg width="32" height="32" viewBox="0 -16.5 99 99" xmlns="http://www.w3.org/2000/svg" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path fill="#EBECED" d="M97.99 28.692a8.952 8.952 0 0 0-3.641-3.746l.016-.01L46.687 0 .004 23.998l.149.084 47.351 24.836c4.395 2.305 6.104 7.766 3.82 12.197a8.967 8.967 0 0 1-3.117 3.426l-.062.081-.041.03 47.781-24.979c3.08-2.666 4.06-7.197 2.105-10.981z"></path><path fill="#BDC3C7" d="M47.504 48.918L0 24.001v20.39l39.235 20.58a8.88 8.88 0 0 0 4.127 1.021 8.954 8.954 0 0 0 7.962-4.875c2.283-4.433.574-9.894-3.82-12.199z"></path><path fill="#7E8B8C" d="M18.37 22.306l4.574 2.305-7.688-.736-2.387 1.202 8.27 4.164 2.402-1.21-4.539-2.287 7.637.729 2.408-1.213-8.27-4.164-2.407 1.21zm13.058-.133l-1.631-.82 3.977-2.002-1.688-.851-3.977 2.002-1.312-.661 4.285-2.158-1.766-.89-6.848 3.448 8.27 4.164 6.973-3.512-1.873-.942-4.41 2.222zm7.694-10.319l3.748 2.771-5.906-1.683-2.418 1.218 3.352 2.976-5.503-1.892-2.427 1.222 10.107 3.238 2.506-1.262-3.762-3.35 6.656 1.892 2.506-1.263-6.445-5.082-2.414 1.215zm16.91-1.419c-.154-.373-.496-.692-1.027-.959-.45-.229-.969-.377-1.553-.45-.586-.073-1.242-.05-1.974.069-.73.119-1.772.398-3.13.84-.545.181-.934.273-1.162.279-.229.01-.409-.02-.541-.086-.182-.091-.259-.205-.234-.345.025-.14.187-.284.482-.435a2.722 2.722 0 0 1 1.104-.299c.373-.019.778.051 1.215.205l2.269-1.283c-.963-.379-1.917-.527-2.862-.445-.949.081-1.951.388-3.008.92-.862.434-1.433.829-1.71 1.188-.277.357-.352.694-.22 1.008.132.314.409.58.835.793.646.326 1.419.474 2.316.44.896-.03 2.029-.265 3.401-.702.834-.269 1.431-.408 1.787-.416.356-.011.646.039.856.146.228.113.324.264.299.449-.024.185-.223.369-.586.554a3.116 3.116 0 0 1-1.631.315c-.369-.023-.774-.121-1.225-.293l-2.277 1.301c.904.385 1.899.576 2.981.576 1.082 0 2.328-.354 3.733-1.062.802-.403 1.349-.796 1.644-1.178.302-.378.372-.757.218-1.13z"></path><path fill="#BDC2C6" d="M64.223 15.245L27.79 33.593l2.666 1.343 36.435-18.349-2.668-1.342zM34.01 36.725l7.998 4.026 10.662-5.369-7.998-4.027-10.662 5.37zm17.772-6.266L73.107 19.72l-2.666-1.343-21.325 10.74 2.666 1.342zm23.991-9.397l-21.326 10.74 2.666 1.344 21.326-10.74-2.666-1.344z"></path><path fill="#7E8B8C" d="M42.028 55.029L0 32.597v2.292l41.123 21.946a.956.956 0 0 0 .451.114c.354 0 .697-.2.873-.549a1.034 1.034 0 0 0-.419-1.371z"></path></g></svg> -->
      
      <!-- <svg width="32" height="32" viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg">
        <g fill="none" fillRule="evenodd">
          <path
            d="M10 0h12a10 10 0 0110 10v12a10 10 0 01-10 10H10A10 10 0 010 22V10A10 10 0 0110 0z"
            fill="#FFF"
          />
          <path
            d="M5.3 10.6l10.4 6v11.1l-10.4-6v-11zm11.4-6.2l9.7 5.5-9.7 5.6V4.4z"
            fill="#555AB9"
          />
          <path
            d="M27.2 10.6v11.2l-10.5 6V16.5l10.5-6zM15.7 4.4v11L6 10l9.7-5.5z"
            fill="#91BAF8"
          />
        </g>
      </svg> -->
      <h1>{title}</h1>
    </div>
    <div>
      {#if supportuser && user}
        <apint-button label="Log out" type="primary"></apint-button>
      {:else if supportuser}
        <apint-button type="secondary" label="Log in"></apint-button><apint-button type="primary" label="Sign up"></apint-button>
      {/if}
    </div>
  </div>
</header>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    padding: 15px 20px;
    font-family: 'Nunito Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  }

  .header svg {
    display: inline-block;
    vertical-align: top;
  }

  .header h1 {
    display: inline-block;
    vertical-align: top;
    margin: 6px 0 6px 10px;
    font-weight: 700;
    font-size: 20px;
    line-height: 1;
  }

  .header button + button {
    margin-left: 10px;
  }

  .header .welcome {
    margin-right: 10px;
    color: #333;
    font-size: 14px;
  }
</style>