<template>
  <div id="app">
    <v-layout wrap>
      <v-flex
        v-for="event in events"
        xs12
        md12
        lg6
        pa-3
        :key="event.key"
      >
        <v-card
          xs12
          md12
          lg6
          :height="cardHeight"
          pa-0
          ma-5
        >
          <v-layout
            style="height:inherit;"
            ma-0
            pa-0
          >
            <v-flex pa-3 grow text-xs-left>
              <v-layout
                column
                fill-height
                justify-space-around
              >
                <v-flex><div>00:00</div></v-flex>
                <v-spacer />
                <v-flex
                  style="vertical-align:bottom;"
                >
                  <div>{{ event.customer }}</div>
                </v-flex>
              </v-layout>
            </v-flex>
            <v-spacer />
            <v-flex pa-0 shrink text-xs-right>
              <v-card
                text-xs-center
                :height="cardHeight"
                flat
              >
                <img
                  contain
                  position="right center"
                  :height="cardHeight"
                  :min-height="cardHeight"
                  :src="event.image"
                  text-xs-right
                />
                <div
                  style="position: absolute; bottom: 0; width: 100%; background: #ffffffaa; text-align: center;"
                >
                  {{ event.resource }}
                </div>
              </v-card>
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import EventCard from '@/EventCard.vue'
export default {
  name: 'App',
  components: { 'event-card': EventCard },
  data() {
    return {
      cardHeight: 250,
      events: [
        {
          key: 1,
          customer: 'Sed ut perspiciatis',
          resource: 'unde omnis',
          image:
            'https://www.ludoviccareme.com/files/image_211_image_fr.jpg'
        },
        {
          key: 2,
          customer: 'Sed ut perspiciatis',
          resource: 'unde omnis',
          image:
            'https://sep.yimg.com/ay/artbook/hiroshi-sugimoto-portraits-29.jpg'
        },
        {
          key: 3,
          customer: 'Sed ut perspiciatis',
          resource: 'unde omnis',
          image:
            'https://cdn.shopify.com/s/files/1/0248/2898/products/finalbuild_357ff21f-f8ba-40df-9007-e7d17c944200.jpg?v=1549430832'
        },
        {
          key: 4,
          customer: 'Sed ut perspiciatis',
          resource: 'unde omnis',
          image:
            'https://www.artpeoplegallery.com/wp-content/uploads/2017/04/1ok-800x634.jpg'
        },
        {
          key: 5,
          customer: 'Sed ut perspiciatis',
          resource: 'unde omnis',
          image:
            'http://cdn.lightgalleries.net/4bd5ebfe8d0eb/images/20160318_NYer_WrestlingPortraits_Selects_0028-1.jpg'
        },
        {
          key: 6,
          customer: 'Sed ut perspiciatis',
          resource: 'unde omnis',
          image:
            'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRcDAFkotOrbkpyfl3ffThQovme6iEdxFPy3apIn4VVkn8ZNio01g'
        }
      ]
    }
  }
}
</script>
