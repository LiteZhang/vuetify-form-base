<template>
  <v-container fluid>
    <h4>Vuetify display helpers, allow to control the  
      <a target="_blank" href="https://vuetifyjs.com/en/styles/display">display</a>
      or 
      <a target="_blank" href="https://vuetifyjs.com/en/styles/typography">typography</a>
      or
      <a target="_blank" href="https://vuetifyjs.com/en/styles/spacing">spacing</a>
      of content
    </h4>

    <!-- FORM-BASE-COMPONENT -->
    <v-form-base
      :value="myValue"
      :schema="mySchema"
      :col="6"
      @input="log"
    />
    
    <!-- Stuff   -->   
    <infoline
      :value="myValue"
      :schema="mySchema"
      :path="$options._componentTag"
    />
  </v-container>
</template>

<script>
import VFormBase from '@/components/vFormBase'
import Infoline from '@/components/infoline'
import log from '@/lib'

export default {
  name: 'DisplayHelpers',
  components: { VFormBase, Infoline },
  data () {
    return {
      myValue: {
        name1: 'Float left & Margin-Top',
        name2: 'Typographie & Pad X-Axis',
        name3: 'Visible on sm',
        name4: 'Visible on xs, Margin-Bottom',
      },
      mySchema: {
        name1: { type: 'text', title:'grey lighten-3 float-left mt-6', class:'grey lighten-3 float-left mt-6' },
        name2: { type: 'text', title:'title px-4 blue lighten-5', class:'title px-4 blue lighten-5' },
        name3: { type: 'text', title:'d-none d-sm-flex d-md-none red lighten-4', class:'d-none d-sm-flex d-md-none red lighten-4' },
        name4: { type: 'text', title:'caption d-flex d-sm-none green lighten-4 mb-2', class:'caption d-flex d-sm-none green lighten-4 mb-2' },
      }
    }
  },
  methods: {
    log
  }
}
</script>
