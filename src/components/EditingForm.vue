<template>
    <form>
        <h1>{{list[i].value}}</h1>
        <label for="select">Выберите элемент</label>
        <select name="select"  @change="e => selectValue(e.target.value)">
            <option :value="i-1" :key="list[i-1]" v-for="i in list.length" >{{ list[i-1].name }}</option>
        </select>
        <label for="input">Измените его значение</label>
        <input name="input" type="text" v-model="list[i].value"/>
    </form>
</template>

<script>
import { data } from "@/utils/data";

export default {
    data: () => ({
        list: data,
        element: data[0],
        i: 0,
    }),
    methods: {
        selectValue(j) {
            console.log(j)
            this.i = j
        }
    },
}
</script>

<style scoped>
    form {
        display: flex;
        flex-direction: column;
        padding: 20px;

        border-radius: 10px;
        background: #ffffff;
        box-shadow: 0 0 10px 1px rgba(0, 0, 0, 0.25);
    }
    h1 {
        margin: 0 auto 20px;
    }
    select {
        width: 367px;
        border: none;
        outline: none;
        border-bottom: 1px solid grey;
        margin-bottom: 20px;
    }
    input {
        border: none;
        outline: none;
        border-bottom: 1px solid grey;
    }
    label {
        margin-bottom: 5px;
    }
</style>