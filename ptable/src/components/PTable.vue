<script>
  import Cell from './ElementCell.vue'
  import BlankCell from './BlankCell.vue'
  import mendeleev from '../assets/mendeleev.json'

  export default {
    name: 'PTable',
    components: {
      Cell,BlankCell
    },

    mounted(){
      let data = mendeleev["Elements"]
      console.log(Object.keys(data).length)
      for (let i = 0; i < Object.keys(data).length; i++) {
        let element = data[i]
        console.log(element)

        let cell = document.createElement('Cell')
        cell.symbol = element.symbol
        cell.name = element.name
        cell.PN = element.PN
        cell.AR = element.AR
        console.log(cell.symbol, cell.name, cell.PN, cell.AR)
        document.querySelector('.Table').appendChild(cell)
      }
    }
  }

</script>

<template>
  <div class="Table">
    <Cell symbol="H" name="Hydrogen" PN="1" AR="1.0"></Cell>
    <BlankCell></BlankCell>
    <Cell symbol="He" name="Helium" PN="2" AR="4.0"></Cell>
  </div>
</template>

<style>
  .Table {
    display: grid;
    grid-template-columns: repeat(18, 1fr);
    grid-template-rows: repeat(9, 1fr);
    grid-gap: 1px;
  }
</style>