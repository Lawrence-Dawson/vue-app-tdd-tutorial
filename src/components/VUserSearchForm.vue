<script>
export default {
    name: 'UserSearchForm',
    data() {
        return {
            username: ''
        }
    }
}
</script>

<template>
    <form @submit.prevent="$emit('submitted', username)">
        <el-input
          placeholder="Pesquise o usuario"
          v-model="username"
          class="search-form__input"
        >
            <el-button
            class="search-form__button"
            native-type="submit"
            slot="append"
            icon="el-icon-search"
            ></el-button>
        </el-input>
        <input type="text" v-model="username" />
        <button type="submit">Search</button>
    </form>
</template>