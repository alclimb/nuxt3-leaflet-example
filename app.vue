<script lang="ts" setup></script>

<template>
  <div>
    <!-- MEMO: SSR/SSGモードではサーバー上でレンダリングせず、ブラウザでのみレンダリングする -->
    <ClientOnly>
      <!-- MEMO: Lazyを付加することをAppLeafletコンポーネントを遅延読み込みする -->
      <LazyAppLeaflet></LazyAppLeaflet>
    </ClientOnly>
  </div>
</template>
