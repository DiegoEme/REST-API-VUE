<template>
    <footer class="d-flex justify-content-between mt-3">
        <div>
        <h3>Información de Interés</h3>

        <li>Mapa del sitio</li>
        <li>Políticas de provacidad</li>
        <li>Condiciones</li>
        <li><a href="github.com">Github</a></li>
      </div>
      <div>
        <h3>Equipo de desarrollo</h3>

        <li>Efrain Perdomo</li>
        <li>Libny López</li>
        <li>Diego Huertas</li>
      </div>
    </footer>
</template>

<script>
export default {
    name: 'PageFooter'
}
</script>

<style scoped>
footer {
    background-color: darkblue ;
    color: lightgoldenrodyellow;
    padding: 1em;
}

li {
    list-style-type: none;
}
</style>
