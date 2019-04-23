<template>
  <div class="home">
    <ul>
      <li>项目1</li>
      <li>项目2</li>
    </ul>
    <Editor v-model="name"></Editor>
    <table class="ui celled table">
      <thead>
        <tr>
          <th>Name</th>
          <th>Age</th>
          <th>Job</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td data-label="Name">James</td>
          <td data-label="Age">24</td>
          <td data-label="Job">Engineer</td>
        </tr>
        <tr>
          <td data-label="Name">Jill</td>
          <td data-label="Age">26</td>
          <td data-label="Job">Engineer</td>
        </tr>
        <tr>
          <td data-label="Name">Elyse</td>
          <td data-label="Age">24</td>
          <td data-label="Job">Designer</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import Editor from "@/components/Editor.vue";
export default {
  name: "project",
  data: function() {
    return {
      name: "zero"
    };
  },
  components: {
    Editor
  },
    created: function () {
        $.get("https://www.baidu.com/")
    }
};
</script>

<style scoped>
ul {
  text-align: left;
}
</style>

