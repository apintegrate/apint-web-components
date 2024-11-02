<script module>
  import { defineMeta } from '@storybook/addon-svelte-csf';
  import ApintCard from '../lib/ApintCard.svelte';
  import { fn } from '@storybook/test';

  // More on how to set up stories at: https://storybook.js.org/docs/writing-stories
  const { Story } = defineMeta({
    title: 'Stories/ApintCard',
    component: ApintCard,
    tags: ['autodocs'],
    argTypes: {},
    args: {}
  });
</script>

<!-- More on writing stories with args: https://storybook.js.org/docs/writing-stories/args -->
<Story name="Card1" args={{
  title: "My test title",
  image: "https://cdn.britannica.com/10/250610-050-BC5CCDAF/Zebra-finch-Taeniopygia-guttata-bird.jpg",
  bylineleft: "bylineleft",
  bylinerightimage: "https://www.theguardian.com/favicon.ico",
  bylineright: "bylineright",
  description: "My test description",
  href: "https://google.com",
  toplefttext: "2 Day(s) ago"
}} />

<Story name="CardLong" args={{
  title: "My test titleMytestitle My testtitleMy test title My testtitle Mytest title Mytesttitle My test title My test title 2 My test title",
  image: "https://cdn.britannica.com/10/250610-050-BC5CCDAF/Zebra-finch-Taeniopygia-guttata-bird.jpg",
  bylineleft: "bylineleft",
  bylinerightimage: "https://www.theguardian.com/favicon.ico",
  bylineright: "bylineright fds fdsa fdsafdsa",
  description: "My test description My test description My test description My test description My test description My test description My test description My test description My test description My test description My test description",
  href: "https://google.com",
  toplefttext: "fds"
}} />