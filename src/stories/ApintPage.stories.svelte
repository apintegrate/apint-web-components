<script module>
  import { defineMeta } from '@storybook/addon-svelte-csf';
  import ApintPage from '../lib/ApintPage.svelte';
  import ApintCard from '../lib/ApintCard.svelte';

  // More on how to set up stories at: https://storybook.js.org/docs/writing-stories
  const { Story } = defineMeta({
    title: 'Stories/ApintPage',
    component: ApintPage,
    tags: ['autodocs'],
    argTypes: {}
  });
</script>

<!-- More on writing stories with args: https://storybook.js.org/docs/writing-stories/args -->
<Story name="Page simple" args={{title: "test"}}>
  <apint-page title="Apint.org">
    <h2>Test header</h2>
    <ul>
      <li>list item 1</li>
      <li>list item 2</li>
    </ul>
  </apint-page>
</Story>

<Story name="Page with cards" args={{title: "test"}}>
  <apint-page>
    <section class="container_wrap">
      <h2>Birds</h2>
      <apint-card title="My test title" image="https://cdn.britannica.com/10/250610-050-BC5CCDAF/Zebra-finch-Taeniopygia-guttata-bird.jpg" description="My test description" href="https://google.com" toplefttext="2 Day(s) ago"></apint-card>
      <apint-card title="My test title" image="https://cdn.britannica.com/10/250610-050-BC5CCDAF/Zebra-finch-Taeniopygia-guttata-bird.jpg" description="My test description" href="https://google.com" toplefttext="2 Day(s) ago"></apint-card>
      <apint-card title="My test title" image="https://cdn.britannica.com/10/250610-050-BC5CCDAF/Zebra-finch-Taeniopygia-guttata-bird.jpg" description="My test description" href="https://google.com" toplefttext="2 Day(s) ago"></apint-card>
      <apint-card title="My test title" image="https://cdn.britannica.com/10/250610-050-BC5CCDAF/Zebra-finch-Taeniopygia-guttata-bird.jpg" description="My test description" href="https://google.com" toplefttext="2 Day(s) ago"></apint-card>
      <apint-card title="My test title" image="https://cdn.britannica.com/10/250610-050-BC5CCDAF/Zebra-finch-Taeniopygia-guttata-bird.jpg" description="My test description" href="https://google.com" toplefttext="2 Day(s) ago"></apint-card>
    </section>
  </apint-page>
</Story>

<style>
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

</style>