<template>
  <h1>Hello, {{ email }}</h1>
</template>

<script>
export default {
  asyncData ({ $axios, params }) {
    return $axios.$get(`http://backend:3000/users/${params.id}`).then((res) => {
      return { email: res.email }
    })
  }
}
</script>
