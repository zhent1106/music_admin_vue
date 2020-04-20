<template>
  <div>
    <span
      v-for="(item, index) in permissions"
      :key="index"
      class="gutter"
    >
      <mu-button
        color="teal"
        v-if="item === 'music:add'"
      >添加歌单</mu-button>
      <mu-button
        color="success"
        v-if="item === 'music:edit'"
      >编辑歌单</mu-button>
      <mu-button
        color="error"
        v-if="item === 'music:delete'"
      >删除歌单</mu-button>
    </span>
    <!-- <v-card
      max-width="400"
      class="mx-auto"
      style="margin-top:20px"
    >
      <v-container class="pa-1">
        <v-item-group
          v-model="selected"
          multiple
        >
          <v-row>
            <v-col
              v-for="(item, i) in items"
              :key="i"
              cols="12"
              md="6"
            >
              <v-item v-slot:default="{ active, toggle }">
                <v-img
                  :src="`https://cdn.vuetifyjs.com/images/${item.src}`"
                  height="150"
                  class="text-right pa-2"
                  @click="toggle"
                >
                  <v-btn
                    icon
                    dark
                  >
                    <v-icon>
                      {{ active ? 'mdi-heart' : 'mdi-heart-outline' }}
                    </v-icon>
                  </v-btn>
                </v-img>
              </v-item>
            </v-col>
          </v-row>
        </v-item-group>
      </v-container>

    </v-card> -->
    <div class="row">
      <v-card
        class="mx-auto elevation-20 bg-musiclist"
        color="purple"
        style="max-width: 400px;margin-top:20px"
      >
        <v-row justify="space-between">
          <v-col cols="8">
            <v-card-title primary-title>
              <div>
                <div class="headline">Halycon Days</div>
                <div>Ellie Goulding</div>
                <div>(2013)</div>
              </div>
            </v-card-title>
          </v-col>
          <v-img
            class="shrink ma-2"
            contain
            height="125px"
            src="https://cdn.vuetifyjs.com/images/cards/halcyon.png"
            style="flex-basis: 125px"
          ></v-img>
        </v-row>
        <v-divider></v-divider>
        <v-card-actions class="pa-4">
          Rate this MusicList
          <v-spacer></v-spacer>
          <span class="grey--text text--lighten-2 caption mr-2">
            ({{ rating }})
          </span>
          <v-rating
            v-model="rating"
            background-color="white"
            color="yellow accent-4"
            dense
            half-increments
            hover
            size="18"
          ></v-rating>
        </v-card-actions>
      </v-card>
      <v-card
        class="mx-auto elevation-20 bg-musiclist"
        color="purple"
        style="max-width: 400px;margin-top:20px;margin-left:20px"
      >
        <v-row justify="space-between">
          <v-col cols="8">
            <v-card-title primary-title>
              <div>
                <div class="headline">Love Story</div>
                <div>Taylor Swift</div>
                <div>(2008)</div>
              </div>
            </v-card-title>
          </v-col>
          <v-img
            class="shrink ma-2"
            contain
            height="125px"
            src="https://p2.music.126.net/cJelfF3l-BEyiAemf8jkeA==/109951163935914650.jpg"
            style="flex-basis: 125px"
          ></v-img>
        </v-row>
        <v-divider dark></v-divider>
        <v-card-actions class="pa-4">
          Rate this MusicList
          <v-spacer></v-spacer>
          <span class="grey--text text--lighten-2 caption mr-2">
            ({{ rating1 }})
          </span>
          <v-rating
            v-model="rating1"
            background-color="white"
            color="yellow accent-4"
            dense
            half-increments
            hover
            size="18"
          ></v-rating>
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MusicList',
  data: () => ({
    rating: 4.3,
    rating1: 5.0
  }),
  // data: () => ({
  //   rating: 4.3
  //   // items: [
  //   //   {
  //   //     src: 'backgrounds/bg.jpg'
  //   //   },
  //   //   {
  //   //     src: 'backgrounds/md.jpg'
  //   //   },
  //   //   {
  //   //     src: 'backgrounds/bg-2.jpg'
  //   //   },
  //   //   {
  //   //     src: 'backgrounds/md2.jpg'
  //   //   }
  //   // ],
  //   // selected: []
  // }),
  created() {
    this.permissions = this.$store.state.menuList[1].subMenus[1].permissions
    console.log(this.permissions)
  }
}
</script>

<style scoped lang="scss">
.row {
  display: flex;
  flex-wrap: wrap;
}
.bg-musiclist {
  background-color: purple;
}
</style>
