<template>
    <div>
        <h1 style="text-align: center;">Quản lý điện thoại</h1>

        <a-form class="mt-5" :model="dienThoai" :ref="formRef" :labelCol="{offset:4, span:4}" :wrapperCol="{span:10}">
          <a-form-item label="Ten">
            <a-input v-model:value="ds.ten"></a-input>
          </a-form-item>
          <a-form-item label="Hang">
            <a-select v-model:value="ds.hang">
              <a-select-option :key="index" :value="hang" v-for="(hang, index) in hangs">{{ hang }}</a-select-option>
            </a-select> 
          </a-form-item>
          <a-form-item label="Dung luong">
            <a-select v-model:value="ds.dungluong">
              <a-select-option :key="index" :value="dl" v-for="(dl, index) in dungluongs">{{ dl }}</a-select-option>
            </a-select>
          </a-form-item>
          <a-form-item label="Gia">
            <a-input-number v-model:value="ds.gia"></a-input-number>
          </a-form-item>
          <a-form-item :wrapperCol="{offset:8, span:4}">
            <a-button type="primary">Add</a-button>
          </a-form-item>
        </a-form>
        <a-table :dataSource="ds" :columns="cols" :pagination="false">
            <template #bodyCell="{ column, record }">
                <a-button v-if="column.key === 'act'" type="link">Detail</a-button>
            </template>
        </a-table>  
    </div>
</template>

<script setup>
import { reactive, ref } from 'vue';

const formRef = ref();

const hangs = ['SamSung','Apple','Oppo'];

const dungluongs = ['64GB','128GB','256GB','512GB','1TB'];

const ds = reactive([
    {
        id: 1,
        ten: 'Iphone 17 pro max',
        hang: 'Apple',
        dungluong: '512gb',
        gia: 2000
    },
])

const cols = [
    {
        title: "ID",
        dataIndex: "id",
    },
    {
        title: "Ten",
        dataIndex: "ten",
    },
    {
        title: "Hang",
        dataIndex: "hang",
    },
    {
        title: "Dung luong",
        dataIndex: "dungluong",
    },
    {
        title: "Gia",
        dataIndex: "gia",
    },
    {
        title: "Hanh dong",
        key: 'act'
    },
];

const 

</script>

<style scoped></style>