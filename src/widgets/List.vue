
<template>
  <section class="excursion-list d-flex flex-column">
    <Tile
      class="excursion-list__tile"
      v-for="excursion of listMock"
      :key="excursion.id"
      :name="excursion.name"
      :info="Object.values(excludeNameAndId(excursion)).filter(Boolean)"
    />
  </section>
</template>

<script>
import Tile from './components/Tile.vue';

export default {
  name: 'List',
  data() {
    return {
      listMock: [
        {
          id: 1,
          rating: {
            value: 5,
            iconName: 'mdi-star-outline',
          },
          type: {
            value: '«Фридландские ворота»',
          },
          date: {
            value: '1,2 км от вас',
          },

        },
        {
          id: 2,
          rating: {
            value: 5,
            iconName: 'mdi-star-outline',
          },
          type: {
            value: '«Фридландские ворота»',
          },
          date: {
            value: '1,2 км от вас',
          },
        },
        {
          id: 3,
          rating: {
            value: 5,
            iconName: 'mdi-star-outline',
          },
          type: {
            value: '«Фридландские ворота»',
          },
          date: {
            value: '1,2 км от вас',
          },
        },
        {
          id: 4,
          rating: {
            value: 5,
            iconName: 'mdi-star-outline',
          },
          type: {
            value: '«Фридландские ворота»',
          },
          date: {
            value: '1,2 км от вас',
          },
        },
      ],
    };
  },
  methods: {
    excludeNameAndId(excursion) {
      const {name, id, ...rest} = excursion;
      return rest;
    },
  },
  components: {
    Tile,
  },
};
</script>
