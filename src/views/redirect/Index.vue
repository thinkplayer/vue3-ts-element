<template>无当前路由</template>
<script lang="ts">
import { defineComponent } from "vue";
import { useRoute, useRouter } from "vue-router";

export default defineComponent({
  created() {
    const { params, query } = useRoute();
    const { path } = params;
    console.log(
      "%c 🍗 params: ",
      "font-size:20px;background-color: #7F2B82;color:#fff;",
      params
    );

    useRouter()
      .replace({
        path: "/" + path,
        query,
      })
      .catch((err) => {
        console.log(
          "%c 🍑 err: ",
          "font-size:20px;background-color: #4b4b4b;color:#fff;",
          err
        );
      });
  },
});
</script>
