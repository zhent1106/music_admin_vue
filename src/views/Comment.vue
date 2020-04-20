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
      >添加评论</mu-button>
      <mu-button
        color="error"
        v-if="item === 'music:delete'"
      >删除评论</mu-button>
    </span>
    <div class="row">
      <v-card
        class="mx-auto"
        color="#26c6da"
        dark
        max-width="400"
        style="margin-top:20px"
      >
        <v-card-title>
          <div class="text-center">
            <v-rating v-model="rating"></v-rating>
          </div>
        </v-card-title>

        <v-card-text class="headline font-weight-bold">
          "Turns out semicolon-less style is easier and safer in TS because most gotcha edge cases are type invalid as well."
        </v-card-text>

        <v-card-actions>
          <v-list-item class="grow">
            <v-list-item-avatar color="grey darken-3">
              <v-img
                class="elevation-6"
                src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
              ></v-img>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Evan You</v-list-item-title>
            </v-list-item-content>

            <v-row
              align="center"
              justify="end"
            >
              <v-icon class="mr-1">mdi-heart</v-icon>
              <span class="subheading mr-2">256</span>
              <span class="mr-1">·</span>
              <v-icon class="mr-1">mdi-share-variant</v-icon>
              <span class="subheading">45</span>
            </v-row>
          </v-list-item>
        </v-card-actions>
      </v-card>
      <v-card
        class="mx-auto"
        color="#26c6da"
        dark
        max-width="400"
        style="margin-top:20px;margin-left:30px"
      >
        <v-card-title>
          <div class="text-center">
            <v-rating v-model="rating"></v-rating>
          </div>
        </v-card-title>

        <v-card-text class="headline font-weight-bold">
          "Turns out semicolon-less style is easier and safer in TS because most gotcha edge cases are type invalid as well."
        </v-card-text>

        <v-card-actions>
          <v-list-item class="grow">
            <v-list-item-avatar color="grey darken-3">
              <v-img
                class="elevation-6"
                src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
              ></v-img>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Evan You</v-list-item-title>
            </v-list-item-content>

            <v-row
              align="center"
              justify="end"
            >
              <v-icon class="mr-1">mdi-heart</v-icon>
              <span class="subheading mr-2">256</span>
              <span class="mr-1">·</span>
              <v-icon class="mr-1">mdi-share-variant</v-icon>
              <span class="subheading">45</span>
            </v-row>
          </v-list-item>
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Comment',
  data: () => ({
    rating: 3
  }),
  created() {
    this.permissions = this.$store.state.menuList[1].subMenus[1].permissions
    console.log(this.permissions)
  }
}
</script>

<style lang="scss" scoped>
.row {
  display: flex;
  flex-wrap: wrap;
}
</style>
