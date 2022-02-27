<template lang="">
    
    <!-- Создание поста -->

    <form @submit.prevent>
      <h4>Создание поста</h4>
      <input
        v-model="post.title"
        class="form-create-input"
        type="text"
        placeholder="Название"
      />
      <input
        v-model="post.body"
        class="form-create-input"
        type="text"
        placeholder="Описание"
      />
      <button class="form-create-btn" >Создать</button>
    </form>

</template>
<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
};
</script>
<style scoped>
form {
  display: flex;
  flex-direction: column;
  /* justify-content:space-around; */
}

.form-create-input {
  /* width: 100px; */
  border: 1px solid black;
  padding: 10px 15px;
  margin-top: 15px;
}
.form-create-btn {
  margin-top: 15px;
  /* position: fixed; */
  width: 100px;
  /* margin: 0 auto; */
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: black;
  border: 1px solid black;
}
</style>