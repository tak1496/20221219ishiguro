<template>
  <div class="students">
    <div class="student_list">
      <h2>生徒一覧</h2>
      <ul v-for="(student, index) in students">
        <li>
          <NuxtLink :to="`/students/${index}`">{{ student.name }}</NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
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
.students {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.student_list {
  display: block;
}
</style>