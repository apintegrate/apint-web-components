
<svelte:options customElement="apint-page" />

<script>
  import ApintHeader from "./ApintHeader.svelte";

  const { title="Apint.org" } = $props();
</script>

<article>
  <apint-header title={title}></apint-header>

  <section class="page">
    <slot />
  </section>
</article>

<style>
  .page {
    margin: 0 auto;
    padding: 14px 20px;
    max-width: 944px;
    color: #333;
    font-size: 14px;
    line-height: 24px;
    font-family: 'Nunito Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  }

  h2 {
    display: inline-block;
    vertical-align: top;
    font-weight: 700;
    font-size: 32px;
    line-height: 1;
    width: 100%;
    margin-left: 10px;
  }

  .container_wrap {
    display: flex;
    flex-flow: row wrap;
    margin: 4px 4px 14px 4px;
    width: 100%;
    justify-content: center;
  }

  .page p {
    margin: 1em 0;
  }

  .page a {
    color: #1ea7fd;
    text-decoration: none;
  }

  .page ul {
    margin: 1em 0;
    padding-left: 30px;
  }

  .page li {
    margin-bottom: 8px;
  }

  .page .tip {
    display: inline-block;
    vertical-align: top;
    margin-right: 10px;
    border-radius: 1em;
    background: #e7fdd8;
    padding: 4px 12px;
    color: #66bf3c;
    font-weight: 700;
    font-size: 11px;
    line-height: 12px;
  }

  .page .tip-wrapper {
    margin-top: 40px;
    margin-bottom: 40px;
    font-size: 13px;
    line-height: 20px;
  }

  .page .tip-wrapper svg {
    display: inline-block;
    vertical-align: top;
    margin-top: 3px;
    margin-right: 4px;
    width: 12px;
    height: 12px;
  }

  .page .tip-wrapper svg path {
    fill: #1ea7fd;
  }

  @media (width <= 700px) {
    .page {
      padding: 4px 4px;
    }

    .page .container_wrap {
      margin: 4px 0px 4px 0px;
      width: 98%;
      justify-content: center;
    }
  }
</style>