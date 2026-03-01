<template>
    <div>
        <h1 style="text-align: center;">Quản lý điện thoại</h1>

        <a-table :dataSource="ds" :columns="cols" :pagination="false">
            <template #bodyCell="{ column, record }">
                <a-button v-if="column.key === 'act'" type="link">Detail</a-button>
            </template>
        </a-table>
            
    </div>
</template>

<script setup>
import { reactive } from 'vue';

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
]

</script>

<style scoped></style>