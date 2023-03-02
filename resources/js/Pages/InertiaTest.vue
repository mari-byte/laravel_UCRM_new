<script setup>
//import { Link } from "@inertiajs/vue3";
import { Link } from "@inertiajs/inertia-vue3";
import { ref } from "vue";
//import route from "vendor/tightenco/ziggy/src/js";

const newTitle = ref("");
const newContent = ref("");
</script>

<template>
    <p>Inertiaのテストです。</p>
    <br />
    <a href="/">aタグ経由です。</a>
    <br />
    <Link href="/">Linkタグ経由です。</Link>
    <br />
    <Link href="inertia/index">名前付きの確認</Link>
    <br />
    <Link href="inertia/show/1">テンプレートの確認</Link>
    <br />

    <dev class="mb-8"></dev>

    <!-- <input type="text" name="newTitle" v-model="newTitle" />{{ newTitle }}<br />
    <input type="text" name="newContent" v-model="newContent" />{{ newContent
    }}<br />
    <Link
        :href="route('inertia.store')"
        as="button"
        method="post"
        :data="{ title: newTitle, content: newContent }"
        >保存テスト</Link
    > -->

    <input type="text" name="newTitle" v-model="newTitle" />{{ newTitle }}<br />
    <input type="text" name="newContent" v-model="newContent" />{{ newContent }}
    <br />
    <Link
        as="button"
        method="post"
        :href="route('inertia.store')"
        :data="{ title: newTitle, content: newContent }"
        >保存テスト</Link
    >
</template>
