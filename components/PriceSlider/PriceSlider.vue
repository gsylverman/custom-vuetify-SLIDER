<template>
<div>
<v-card flat color="transparent">
    <v-subheader>Default range slider</v-subheader>

    <v-card-text>
      <v-range-slider
        v-model="values"
        thumb-color="#60EA8B"
        thumb-label="always"
        track-color="#33404A"
        color="#33404A"
        :max="1500"
        :min="0"
        :thumb-size="40"
      >
        <template v-slot:thumb-label="props">
          {{`$${props.value}`}}
        </template>    
      </v-range-slider>
    </v-card-text>

  </v-card>
  <div>
      <pre>{{values}}</pre>
  </div>
</div>
  
</template>

<script>
  export default {
    data () {
      return {
        values: [120, 1200]
      }
    }
  }
</script>
