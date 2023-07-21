<template>
    <div>
        <h2>Halo, {{ nama }}</h2>
        <p>Umur kamu: {{ umur }}</p>
    </div>
</template>

<script>
export default {
    props: ['nama', 'umur'], //definisi props "nama" dan "umur"
}
</script>