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
      <g clip-path="url(#clip0_2_2)">
        <path d="M193.576 513.516C157.217 517.594 131.576 497.748 106.075 475.613C69.6258 443.973 47.1641 396.837 77.5571 359.914C106.997 324.149 165.566 315.394 165.566 315.394C165.566 315.394 94.147 324.78 49.6859 285.218C27.0119 265.042 14.2939 238.66 11.1411 208.137C7.08554 168.875 0.471379 88.5414 0.0151147 58.8832C-0.500677 25.3541 12.2093 2.94012 34.3572 0.473397C87.3539 -5.42913 149.61 44.4347 210.108 118.171C268.909 189.839 291.946 240.535 291.946 240.535C291.946 240.535 314.983 189.839 373.784 118.171C434.283 44.4347 496.539 -5.42913 549.535 0.473397C571.683 2.94012 584.393 25.3541 583.877 58.8832C583.421 88.5414 576.807 168.875 572.751 208.137C569.599 238.66 556.881 265.042 534.207 285.218C489.745 324.78 418.327 315.394 418.327 315.394C418.327 315.394 476.896 324.149 506.335 359.914C536.728 396.837 514.267 443.973 477.817 475.613C452.317 497.748 426.675 517.594 390.316 513.516C324.181 506.1 291.946 382.855 291.946 382.855C291.946 382.855 259.711 506.1 193.576 513.516Z" fill="white"/>
      </g>
      <defs>
          <clipPath id="clip0_2_2">
          <rect width="583.892" height="514.052" fill="white"/>
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
      <g clip-path="url(#clip0_2_2)">
        <path d="M193.576 513.516C157.217 517.594 131.576 497.748 106.075 475.613C69.6258 443.973 47.1641 396.837 77.5571 359.914C106.997 324.149 165.566 315.394 165.566 315.394C165.566 315.394 94.147 324.78 49.6859 285.218C27.0119 265.042 14.2939 238.66 11.1411 208.137C7.08554 168.875 0.471379 88.5414 0.0151147 58.8832C-0.500677 25.3541 12.2093 2.94012 34.3572 0.473397C87.3539 -5.42913 149.61 44.4347 210.108 118.171C268.909 189.839 291.946 240.535 291.946 240.535C291.946 240.535 314.983 189.839 373.784 118.171C434.283 44.4347 496.539 -5.42913 549.535 0.473397C571.683 2.94012 584.393 25.3541 583.877 58.8832C583.421 88.5414 576.807 168.875 572.751 208.137C569.599 238.66 556.881 265.042 534.207 285.218C489.745 324.78 418.327 315.394 418.327 315.394C418.327 315.394 476.896 324.149 506.335 359.914C536.728 396.837 514.267 443.973 477.817 475.613C452.317 497.748 426.675 517.594 390.316 513.516C324.181 506.1 291.946 382.855 291.946 382.855C291.946 382.855 259.711 506.1 193.576 513.516Z" fill="white"/>
      </g>
      <defs>
          <clipPath id="clip0_2_2">
          <rect width="583.892" height="514.052" fill="white"/> <!-- this width and height might be the issue -->
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