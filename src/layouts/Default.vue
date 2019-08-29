<template>
  <div class="font-sans p-4 text-gray-900 max-w-xl">
    <header class="mb-8">
      <nav>
        <g-link
          to="/"
          class="uppercase tracking-wider text-sm font-medium mr-4 pb-1"
          :class="{
            'text-gray-600 hover:text-gray-900': $route.path !== '/',
            'border-b-2 border-gray-900': $route.path === '/'
          }">{{ $static.metaData.siteName }}</g-link>
        <g-link
          to="/prayers"
          class="uppercase tracking-wider text-sm font-medium pb-1"
          :class="{
            'text-gray-600 hover:text-gray-900': $route.path !== '/prayers',
            'border-b-2 border-gray-900': $route.path === '/prayers'
            }">Prayers</g-link>
      </nav>
    </header>
    
    <slot/>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>