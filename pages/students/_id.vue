<template>
  <div class="student_id">
    <div>
      <h1>{{ students[student_id].name }}</h1>
      <NuxtLink to="/students">生徒一覧へ戻る</NuxtLink>｜
      <NuxtLink to="/">トップページへ</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    return /^\d+$/.test(params.id)
  },
  data() {
    return {
      student_id: this.$route.params.id,
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
    };
  }
};
</script>

<style>
.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>