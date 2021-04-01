<template>
  <!-- <editorwang @change="changeWang"></editorwang> -->
  <div style="width: 100%; height: 100%">
    <el-button type="text" @click="dialogVisible = true"
      >点击打开 Dialog</el-button
    >
    <el-dialog title="提示" :visible.sync="dialogVisible" width="30%">
      <div>
        <editorwang @change="changeWang"></editorwang>
      </div>
    </el-dialog>
  </div>
</template>

<script>
// @ is an alias to /src
import editorwang from "@/components/wangEnditor";
export default {
  name: "Home",
  data() {
    return {
      dialogVisible: false,
    };
  },
  components: {
    editorwang,
  },
  methods: {
    changeWang(html) {
      console.log(html);
    },
  },

  mounted() {},
};
</script>



