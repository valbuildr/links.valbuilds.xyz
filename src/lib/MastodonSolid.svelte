<script lang="ts">
    import { getContext } from 'svelte';
    import { twMerge } from 'tailwind-merge';
    type TitleType = {
      id?: string;
      title?: string;
    };
    type DescType = {
      id?: string;
      desc?: string;
    };
  
    interface BaseProps {
      size?: 'xs' | 'sm' | 'md' | 'lg' | 'xl';
      role?: string;
      color?: string;
      withEvents?: boolean;
      onclick?: (event: MouseEvent) => void;
      onkeydown?: (event: KeyboardEvent) => void;
      onkeyup?: (event: KeyboardEvent) => void;
    }
  
    interface CtxType extends BaseProps {}
    interface Props extends BaseProps {
      title?: TitleType;
      desc?: DescType;
      ariaLabel?: string;
      size?: 'xs' | 'sm' | 'md' | 'lg' | 'xl';
    }
  
    const ctx: CtxType = getContext('iconCtx') ?? {};
    const sizes = {
      xs: 'w-3 h-3',
      sm: 'w-4 h-4',
      md: 'w-5 h-5',
      lg: 'w-6 h-6',
      xl: 'w-8 h-8'
    };
  
    export let size: Props['size'] = ctx.size || 'md';
    export let role: Props['role'] = ctx.role || 'img';
    export let color: Props['color'] = ctx.color || 'currentColor';
    export let withEvents: Props['withEvents'] = ctx.withEvents || false;
    export let title: TitleType = {};
    export let desc: DescType = {};
  
    let ariaDescribedby = `${title.id || ''} ${desc.id || ''}`;
    let hasDescription = false;
  
    $: if (title.id || desc.id) {
      hasDescription = true;
    } else {
      hasDescription = false;
    }
    export let ariaLabel = 'apple solid';
  </script>
  
  {#if withEvents}
    <svg
      xmlns="http://www.w3.org/2000/svg"
      fill={color}
      {...$$restProps}
      class={twMerge('shrink-0', sizes[size ?? 'md'], $$props.class)}
      {role}
      aria-label={ariaLabel}
      aria-describedby={hasDescription ? ariaDescribedby : undefined}
      viewBox="0 0 24 24"
      on:click
      on:keydown
      on:keyup
      on:focus
      on:blur
      on:mouseenter
      on:mouseleave
      on:mouseover
      on:mouseout
    >
      {#if title.id && title.title}
        <title id={title.id}>{title.title}</title>
      {/if}
      {#if desc.id && desc.desc}
        <desc id={desc.id}>{desc.desc}</desc>
      {/if}
      <g clip-path="url(#clip0_3_2)">
        <path fill-rule="evenodd" clip-rule="evenodd" d="M164.528 188.625C195.536 184.923 222.535 165.817 225.928 148.36C231.275 120.86 230.833 81.2507 230.833 81.2507C230.833 27.5653 195.66 11.8293 195.66 11.8293C177.925 3.684 147.472 0.258667 115.833 0H115.056C83.4172 0.258667 52.9838 3.684 35.2478 11.8293C35.2478 11.8293 0.073168 27.5653 0.073168 81.2507C0.073168 84.5053 0.0563463 87.9285 0.0388344 91.4921C-0.00979984 101.389 -0.0637576 112.37 0.222501 123.831C1.49983 176.332 9.84784 228.075 58.3892 240.923C80.7705 246.847 99.9865 248.087 115.463 247.236C143.528 245.68 159.283 237.22 159.283 237.22L158.357 216.857C158.357 216.857 138.301 223.181 115.777 222.411C93.4612 221.645 69.9025 220.004 66.2932 192.605C65.9598 190.199 65.7932 187.625 65.7932 184.923C65.7932 184.923 87.6998 190.277 115.463 191.549C132.439 192.328 148.359 190.555 164.528 188.625ZM189.344 150.419V85.4155C189.344 72.1301 185.961 61.5728 179.168 53.7621C172.16 45.9515 162.984 41.9475 151.594 41.9475C138.414 41.9475 128.434 47.0128 121.837 57.1448L115.421 67.8981L109.006 57.1448C102.408 47.0128 92.4278 41.9475 79.2491 41.9475C67.8585 41.9475 58.6825 45.9515 51.6758 53.7621C44.8811 61.5728 41.4985 72.1301 41.4985 85.4155V150.419H67.2518V87.3261C67.2518 74.0261 72.8478 67.2755 84.0411 67.2755C96.4171 67.2755 102.621 75.2835 102.621 91.1181V125.653H128.222V91.1181C128.222 75.2835 134.425 67.2755 146.801 67.2755C157.994 67.2755 163.59 74.0261 163.59 87.3261V150.419H189.344Z" fill="white"/>
      </g>
      <defs>
          <clipPath id="clip0_3_2">
          <rect width="230.842" height="247.477" fill="white"/> <!-- this width and height might be the issue -->
          </clipPath>
      </defs>
    </svg>
  {:else}
    <svg
      xmlns="http://www.w3.org/2000/svg"
      fill={color}
      {...$$restProps}
      class={twMerge('shrink-0', sizes[size ?? 'md'], $$props.class)}
      {role}
      aria-label={ariaLabel}
      aria-describedby={hasDescription ? ariaDescribedby : undefined}
      viewBox="0 0 24 24"
    >
      {#if title.id && title.title}
        <title id={title.id}>{title.title}</title>
      {/if}
      {#if desc.id && desc.desc}
        <desc id={desc.id}>{desc.desc}</desc>
      {/if}
      <g clip-path="url(#clip0_3_2)">
        <path fill-rule="evenodd" clip-rule="evenodd" d="M164.528 188.625C195.536 184.923 222.535 165.817 225.928 148.36C231.275 120.86 230.833 81.2507 230.833 81.2507C230.833 27.5653 195.66 11.8293 195.66 11.8293C177.925 3.684 147.472 0.258667 115.833 0H115.056C83.4172 0.258667 52.9838 3.684 35.2478 11.8293C35.2478 11.8293 0.073168 27.5653 0.073168 81.2507C0.073168 84.5053 0.0563463 87.9285 0.0388344 91.4921C-0.00979984 101.389 -0.0637576 112.37 0.222501 123.831C1.49983 176.332 9.84784 228.075 58.3892 240.923C80.7705 246.847 99.9865 248.087 115.463 247.236C143.528 245.68 159.283 237.22 159.283 237.22L158.357 216.857C158.357 216.857 138.301 223.181 115.777 222.411C93.4612 221.645 69.9025 220.004 66.2932 192.605C65.9598 190.199 65.7932 187.625 65.7932 184.923C65.7932 184.923 87.6998 190.277 115.463 191.549C132.439 192.328 148.359 190.555 164.528 188.625ZM189.344 150.419V85.4155C189.344 72.1301 185.961 61.5728 179.168 53.7621C172.16 45.9515 162.984 41.9475 151.594 41.9475C138.414 41.9475 128.434 47.0128 121.837 57.1448L115.421 67.8981L109.006 57.1448C102.408 47.0128 92.4278 41.9475 79.2491 41.9475C67.8585 41.9475 58.6825 45.9515 51.6758 53.7621C44.8811 61.5728 41.4985 72.1301 41.4985 85.4155V150.419H67.2518V87.3261C67.2518 74.0261 72.8478 67.2755 84.0411 67.2755C96.4171 67.2755 102.621 75.2835 102.621 91.1181V125.653H128.222V91.1181C128.222 75.2835 134.425 67.2755 146.801 67.2755C157.994 67.2755 163.59 74.0261 163.59 87.3261V150.419H189.344Z" fill="white"/>
      </g>
      <defs>
          <clipPath id="clip0_3_2">
          <rect width="230.842" height="247.477" fill="white"/> <!-- this width and height might be the issue -->
          </clipPath>
      </defs>
    </svg>
  {/if}
  
  <!--
  @component
  [Go to docs](https://flowbite-svelte-icons.codewithshin.com/)
  ## Props
  @prop export let size: Props['size'] = ctx.size || 'md';
  @prop export let role: Props['role'] = ctx.role || 'img';
  @prop export let color: Props['color'] = ctx.color || 'currentColor';
  @prop export let withEvents: Props['withEvents'] = ctx.withEvents || false;
  @prop export let title: TitleType = {};
  @prop export let desc: DescType = {};
  @prop export let ariaLabel = 'mastodon solid';
  -->