<template>
    <div id="secure">
        <div class="card">
            <div class="container">
                <h4><b>Alif Setyakurniawan</b></h4>
                <p>Software Engineer</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Secure',
    }
</script>

<style scoped>
    #secure {
        background-color: #8AD0D6;
        padding: 20px;
        margin-top: 10px;
    }
    .card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 16px;
  width: 700px;
}
</style>