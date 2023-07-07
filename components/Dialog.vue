<template>
    <div>
      <v-dialog
        v-model="dialog"
        width="500"
      >
        <template v-slot:activator="{ on, attrs }">
            <v-btn
                color="white"
                icon
                x-large
                v-bind="attrs"
                v-on="on"
                @click="copyToClipboard()"                                    
            >
                <v-icon
                    x-large
                >
                    mdi-email
                </v-icon>
            </v-btn>
        </template>
  
        <v-card>
          <v-card-title class="text-h5 grey darken-3">
            EMAIL COPIED
          </v-card-title>
  
          <v-card-text class="pa-5 text-subtitle-1 text-justify">
            My contact email was copied successfully. You just need to paste it (ctrl+v) in the "to" field in your email provider if you want to contact me by email.
          </v-card-text>

          <v-card-text class="pa-3 text-subtitle-1 text-right">
           Thank you
          </v-card-text>
  
          <v-divider></v-divider>
  
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              color="red"
              text
              @click="dialog = false"
            >
              Close
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
  </template>

<script>
export default {
  data () {
    return {
      dialog: false,
      email: 'tiagofortalezag@gmail.com'
    }
  },
  methods: {
    copyToClipboard(){
        navigator.clipboard.writeText(this.email)
        .then(() => {
          console.log("Text copied to clipboard");
        })
        .catch((error) => {
          console.error("Failed to copy text to clipboard:", error);
        });
    }
  }
}
</script>