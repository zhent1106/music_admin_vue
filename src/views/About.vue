<template>
  <v-container>
    <v-card
      max-width="375"
      class="mx-auto"
    >
      <v-img
        src="https://upload.jianshu.io/users/upload_avatars/14271572/902a126c-cd1f-4900-be7e-993ac34d36e0?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120"
        height="300px"
        dark
      >
        <v-row class="fill-height">
          <v-card-title>
            <v-btn
              dark
              icon
            >
              <v-icon>mdi-chevron-left</v-icon>
            </v-btn>

            <v-spacer></v-spacer>

            <v-btn
              dark
              icon
              class="mr-4"
            >
              <v-icon>mdi-pencil</v-icon>
            </v-btn>

            <v-btn
              dark
              icon
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-card-title>

          <v-spacer></v-spacer>

          <v-card-title class="white--text pl-12 pt-12">
            <div class="display-1 pl-12 pt-12">zhent</div>
          </v-card-title>
        </v-row>
      </v-img>

      <v-list two-line>
        <v-list-item>
          <v-list-item-icon>
            <v-icon color="indigo">mdi-email</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>zhent1106@163.com</v-list-item-title>
            <v-list-item-subtitle>Mail</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider inset></v-divider>

        <v-list-item>
          <v-list-item-icon>
            <v-icon color="indigo">mdi-map-marker</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>NIIT</v-list-item-title>
            <v-list-item-subtitle>Nanjing,Jiangsu</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {}
  },
  components: {},
  created() {},
  mounted() {},
  methods: {},
  computed: {}
}
</script>
<style scoped lang="scss">
.bottom-gradient {
  background-image: linear-gradient(to top, rgba(0, 0, 0, 0.4) 0%, transparent 72px);
}

.repeating-gradient {
  background-image: repeating-linear-gradient(
    -45deg,
    rgba(255, 0, 0, 0.25),
    rgba(255, 0, 0, 0.25) 5px,
    rgba(0, 0, 255, 0.25) 5px,
    rgba(0, 0, 255, 0.25) 10px
  );
}
</style>
