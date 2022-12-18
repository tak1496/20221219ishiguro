<template>
  <div class="management">
    <table>
      <tr>
        <td colspan="2">
          <h2>生徒管理ページ</h2>
        </td>
      </tr>
      <tr>
        <th>名前</th>
        <th>ID</th>
      </tr>
      <tr v-for="(student, index) in students">
        <td class="td_name">{{ student.name }}</td>
        <td class="td_id">{{ student.id }}</td>
      </tr>
      <tr>
        <td colspan="2">
          <NuxtLink to="/">戻る</NuxtLink>
        </td>
      </tr>
    </table>
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
.management {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

th,
td {
  height: 40px;
}

.td_name {
  width: 150px;
}
</style>