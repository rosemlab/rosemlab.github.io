<template>
  <nav>
    <NuxtLink to="/">Home</NuxtLink>
    <!--    <svg width="1" height="28"><line x1="0" y1="0" x2="0" y2="28" stroke="currentColor"></line></svg>-->
    <NuxtLink to="/authors/roshe">Author</NuxtLink>
  </nav>
</template>

<style lang="postcss" scoped>
nav {
  @apply relative flex justify-center text-center;

  height: 28px;
  margin: 26px;
  /*background: linear-gradient(*/
  /*  to right,*/
  /*  transparent calc(50% - .05rem),*/
  /*  #2c3e50 calc(50% - .05rem),*/
  /*  #2c3e50 calc(50% + .05rem),*/
  /*  transparent calc(50% + .05rem)*/
  /*);*/
  background: url("data:image/svg+xml;utf8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1' height='100%'%3E%3Cline x1='0' y1='0' x2='1' y2='100%' stroke='currentColor'%3E%3C/line%3E%3C/svg%3E")
    center no-repeat;

  & a {
    @apply leading-tight;

    padding: 4px 10px;

    &:hover {
      @apply border-b-0;
    }

    &:first-of-type {
      @apply absolute border-none;

      right: 50%;
    }

    &:last-of-type {
      @apply absolute;

      left: 50%;
    }

    &.link-exact-active {
      @apply font-bold;
    }
  }
}

@media print {
  nav {
    @apply hidden;
  }
}
</style>
