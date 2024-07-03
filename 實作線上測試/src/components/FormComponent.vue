<template>
  <form class="form-container">
    <div>
      <label for="applicant">申請人：</label>
      <input
        type="text"
        placeholder="李長勳"
        id="applicant"
        v-model="form.applicant"
        :maxlength="10"
        :disabled="form.locked"
      />
    </div>
    <div>
      <label for="age">年齡：</label>
      <input
        type="number"
        placeholder="28"
        id="age"
        v-model="form.age"
        :min="18"
        :max="38"
        :disabled="form.locked"
      />
    </div>
    <div>
      <label for="department">部門：</label>
      <select id="department" v-model="form.department" :disabled="form.locked">
        <option value="人事部">人事部</option>
        <option value="會計部">會計部</option>
        <option value="資訊部">資訊部</option>
      </select>
    </div>
    <div>
      <label>性別：</label>
      <label
        ><input
          type="radio"
          v-model="form.gender"
          value="男"
          :disabled="form.locked"
        />
        男</label
      >
      <label
        ><input
          type="radio"
          v-model="form.gender"
          value="女"
          :disabled="form.locked"
        />
        女</label
      >
    </div>
    <div>
      <label><input type="checkbox" v-model="form.locked" /> 鎖定</label>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      form: {
        department: "資訊部",
        gender: "男",
        locked: false,
      },
    };
  },
};
</script>

<style scoped>
.form-container {
  border: 1px solid darkblue;
  border-radius: 15px;
  padding: 50px;
  width: 350px;
  margin: 50px auto;
}

form div {
  margin-bottom: 10px;
}

form label {
  display: inline-block;
  width: 60px;
}
</style>
