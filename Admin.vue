<template>
    <v-tabs vertical 
    height="1200px"
    background-color="#99CCFF"
    color="#006699">
      <v-tab>
        <v-icon left>
          mdi-file-document-outline
        </v-icon>
      Просмотр отчетов
      </v-tab>
      <v-tab>
        <v-icon left>
          mdi-hammer-wrench
        </v-icon>
      Администрирование У/З
      </v-tab>
      <v-tab-item>

    <v-card-title>Выберите необходимый отчет</v-card-title>

  <v-row>
    <v-col
      cols="12"
      class="py-1"
    >
      <v-btn-toggle
      v-model="text"
        tile
        color="#006699"
        group
      >
        <v-btn value="lefts">
          <span class="hidden-sm-and-down">Открыть</span>
        </v-btn>
        <v-btn value="left">
          <span class="hidden-sm-and-down">Отправить на печать</span>
        </v-btn>

        <v-btn value="center">
          <span class="hidden-sm-and-down">Импортировать</span>
        </v-btn>

        <v-btn value="right">
          <span class="hidden-sm-and-down">Редактировать</span>
        </v-btn>

        <v-btn value="justify">
          <span class="hidden-sm-and-down">Удалить</span>
        </v-btn>
      </v-btn-toggle>
    </v-col>
  </v-row>
   <v-card
    class="mx-auto"
    max-width="100%"
    tile
    elevation=0
  >
    <v-list dense>
      <v-list-item-group
        v-model="selectedItem"
        color="#006699"
      >
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>

    <v-divider class="mx-4"></v-divider>

      </v-tab-item>
      <v-tab-item>

<v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-center">
          </th>
          <th class="text-left">
            ФИО
          </th>
          <th class="text-left">

          </th>
        </tr>
      </thead>
      <tbody>
        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Иванов Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Кирсов Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Деревин Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Киселевич Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Жаворонков Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Георгиев Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Сергеев Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>
<tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Деревин Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Киселевич Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Жаворонков Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr><tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Деревин Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Киселевич Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Жаворонков Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr><tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Деревин Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Киселевич Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Жаворонков Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr><tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Деревин Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Киселевич Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Жаворонков Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr><tr
        >
          <td>
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Деревин Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Киселевич Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>

        <tr
        >
          <td>
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        /></td>
          <td>Жаворонков Иван Иванович</td>
          <td>
            <v-btn
            elevation=0>
              Редактировать
            </v-btn></td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>

      </v-tab-item>
      <v-tab-item>

      </v-tab-item>
    </v-tabs>
</template>
<script>
  export default {
    data: () => ({
      dialog: '',
      text: 'center',
      icon: 'justify',
      toggle_none: null,
      toggle_one: 0,
      toggle_exclusive: 2,
      toggle_multiple: [0, 1, 2],
      selectedItem: 1,
      desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
          },
          {
            name: 'Eclair',
            calories: 262,
          },
          {
            name: 'Cupcake',
            calories: 305,
          },
          {
            name: 'Gingerbread',
            calories: 356,
          },
          {
            name: 'Jelly bean',
            calories: 375,
          },
          {
            name: 'Lollipop',
            calories: 392,
          },
          {
            name: 'Honeycomb',
            calories: 408,
          },
          {
            name: 'Donut',
            calories: 452,
          },
          {
            name: 'KitKat',
            calories: 518,
          },
        ],
      items: [
        { text: 'Отчет по выданным финансовым продуктам за последний календарный месяц', icon: 'mdi-clock' },
        { text: 'Отчет по всем обслуживаемым физическим лицам', icon: 'mdi-account' },
        { text: 'Отчет по всем денежным суммам в обороте за текущий финансовый год', icon: 'mdi-currency-usd' },
      ],
    }),
  }
</script>