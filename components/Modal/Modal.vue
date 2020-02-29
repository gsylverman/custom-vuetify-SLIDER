<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" scrollable max-width="300px">
      <template v-slot:activator="{ on }">
        <v-btn style="background:lightblue !important; margin-left:0 !important;" color="primary" dark v-on="on">Open Dialog</v-btn>
      </template>

         <v-card>
            <v-btn
            absolute
            permanent
            style="min-width:0"
            right
            color="blue darken-1"
            text
            @click="dialog = false"
            >X</v-btn>
            <v-card-title>Select Option</v-card-title>

            <v-card-text style="height: 300px;">
                <v-radio-group v-model="dialogm1" column>
                    <v-radio label="Option 1" value="option1"></v-radio>
                    <v-radio label="Option 2" value="option2"></v-radio>
                    <v-radio label="Option 3" value="option3"></v-radio>
                    <v-radio label="Option 4" value="option4"></v-radio>
                    <v-radio label="Option 5" value="option5"></v-radio>
                    <v-radio label="Option 6" value="option6"></v-radio>
                    <v-radio label="Option 7" value="option7"></v-radio>
                    <div>{{some}}</div>
                </v-radio-group>
            </v-card-text>
            <v-divider></v-divider>
        </v-card>
    </v-dialog>
  </v-row>
</template>

  <script>
export default {
  props: ["some"],
  data() {
    return {
      dialogm1: "",
      dialog: false
    };
  }
};
</script>

<style scoped>
.v-btn:not(.v-btn--round).v-size--default {
  padding: 2px;
}
.v-application .justify-center {
    justify-content:flex-start !important;
    display: inline;
    position: relative;
    left: 25px;

}
</style>