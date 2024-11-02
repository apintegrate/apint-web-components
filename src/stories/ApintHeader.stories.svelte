<script module>
  import { defineMeta } from '@storybook/addon-svelte-csf';
  import ApintHeader from '../lib/ApintHeader.svelte';
  import { fn } from '@storybook/test';

  // More on how to set up stories at: https://storybook.js.org/docs/writing-stories
  const { Story } = defineMeta({
    title: 'Stories/ApintHeader',
    component: ApintHeader,
    tags: ['autodocs'],
    argTypes: {
      title: { 
        control: { type: 'text' }
      },
      supportuser: {
        control: {type: 'boolean'}
      },
      user: {
        control: {type: 'object'}
      }
    }
  });
</script>

<!-- More on writing stories with args: https://storybook.js.org/docs/writing-stories/args -->
<Story name="Signed In" args={{ supportuser: true, user: {name: "John Doe"}}}></Story>

<Story name="Signed Out" args={{ supportuser: true }}></Story>
