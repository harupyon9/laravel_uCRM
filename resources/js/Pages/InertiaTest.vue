<script setup>
import { Link } from '@inertiajs/inertia-vue3';
import { ref } from 'vue';

const newTitle = ref('');
const newContent = ref('');
</script>

<template>
    <div class="m-8">
        <input type="text" name="newTitle" v-model="newTitle" />{{ newTitle }}<br />
        <input type="text" name="newContent" v-model="newContent" />{{ newContent
        }}<br />
        <Link
            as="button"
            method="post"
            :href="route('inertia.store')"
            :data="{ title: newTitle, content: newContent }">保存テスト
        </Link>
    </div>
</template>
