<template>
<div>
    <v-tabs vertical 
    height="1200px"
    background-color="#99CCFF"
    color="#006699">
      <v-tab>
        <v-icon left>
          mdi-account
        </v-icon>
        Личный кабинет
      </v-tab>
      <v-tab>
        <v-icon left>
          mdi-account-multiple-outline
        </v-icon>
      Список всех заемщиков
      </v-tab>
      <v-tab>
        <v-icon left>
          mdi-cash-100
        </v-icon>
      Баланс лицевого счета
      </v-tab>
      <v-tab-item>
    <v-card-title>Ваш рейтинг кредитора</v-card-title>
    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="3.5"
          color="amber"
          dense
          half-increments
          readonly
          size="30"
        ></v-rating>
        <div class="grey--text ml-4">
          4.5 (413)
        </div>
      </v-row>
      <div class="my-4 subtitle-1">
        Иванов Иван Иванович
      </div>
      <div>Через 19 дней Ваши данные будут обновлены.</div>
      </v-card-text>
      <v-divider class="mx-4"></v-divider>
      <v-card-title>Список ваших должников:</v-card-title>
      <v-card-text>
      <v-row no-gutters>
      <v-col
        cols="12"
      >
        <v-card
          class="pa-1"
          tile
          elevation="0"
        >
         
       <v-data-table
        item-key="ФИО"
        :headers="headersCHIP"
        :items="dessertsCHIP"
        class="elevation-0"
        hide-default-footer
      >
      </v-data-table>


        </v-card>
      </v-col>
    </v-row>
      </v-card-text>
    </v-tab-item>
    <v-tab-item>
    <v-card-title>Список всех заемщиков</v-card-title>
    <v-card-text>
      <v-row no-gutters>
      <v-col
        cols="12"
      >
        <v-card
          class="pa-1"
          tile
          elevation="0"
        >
              <v-btn
          color="white"
          elevation="1"
              >
                Кредитовать
              </v-btn>
        
              <v-btn
          color="white"
          elevation="1"
              >
                Просмотр карточки сотрудника
              </v-btn>
        
              <v-btn
          color="white"
          elevation="1"
              >
                Убрать из списка
              </v-btn>
        </v-card>
      </v-col>
    </v-row>


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
            Департамент
          </th>
          <th class="text-left">
            Рейтинг
          </th>
          <th class="text-left">
            Никнейм
          </th>
          <th class="text-left">
            Стаж
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
            Департамент развития
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            iavin_1
          </td>
          <td>
            1 год
          </td>
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
            Департамент Дроггери
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            afin_1
          </td>
          <td>
            2 года
          </td>
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
          <td>Тулеев Иван Иванович</td>
          <td>
            Департамент маркетинга
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            dodla_00
          </td>
          <td>
            6 лет
          </td>
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
          <td>Савилов Иван Иванович</td>
          <td>
            Департамент сопровождения
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            feruk_10
          </td>
          <td>
            6 месяцев
          </td>
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
          <td>Диванов Иван Иванович</td>
          <td>
            Департамент транспортной логистики
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            gokil_12
          </td>
          <td>
            4 года
          </td>
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
            Департамент Дроггери
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            afin_1
          </td>
          <td>
            2 года
          </td>
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
          <td>Тулеев Иван Иванович</td>
          <td>
            Департамент маркетинга
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            dodla_00
          </td>
          <td>
            6 лет
          </td>
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
          <td>Савилов Иван Иванович</td>
          <td>
            Департамент сопровождения
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            feruk_10
          </td>
          <td>
            6 месяцев
          </td>
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
          <td>Диванов Иван Иванович</td>
          <td>
            Департамент транспортной логистики
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            gokil_12
          </td>
          <td>
            4 года
          </td>
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
            Департамент Дроггери
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            afin_1
          </td>
          <td>
            2 года
          </td>
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
          <td>Тулеев Иван Иванович</td>
          <td>
            Департамент маркетинга
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            dodla_00
          </td>
          <td>
            6 лет
          </td>
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
          <td>Савилов Иван Иванович</td>
          <td>
            Департамент сопровождения
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            feruk_10
          </td>
          <td>
            6 месяцев
          </td>
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
          <td>Диванов Иван Иванович</td>
          <td>
            Департамент транспортной логистики
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            gokil_12
          </td>
          <td>
            4 года
          </td>
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
            Департамент Дроггери
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            afin_1
          </td>
          <td>
            2 года
          </td>
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
          <td>Тулеев Иван Иванович</td>
          <td>
            Департамент маркетинга
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            dodla_00
          </td>
          <td>
            6 лет
          </td>
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
          <td>Савилов Иван Иванович</td>
          <td>
            Департамент сопровождения
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            feruk_10
          </td>
          <td>
            6 месяцев
          </td>
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
          <td>Диванов Иван Иванович</td>
          <td>
            Департамент транспортной логистики
          </td>
          <td>
            <v-rating
      v-model="rating"
      icon-label="custom icon label text {0} of {1}"
    ></v-rating>
          </td>
          <td>
            gokil_12
          </td>
          <td>
            4 года
          </td>
        </tr>




      </tbody>
    </template>
  </v-simple-table>
      
      </v-card-text>
      
    </v-tab-item>
    <v-tab-item>


<v-card
    class="mx-auto"
    max-width="100%"
  >
    <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title class="headline">
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="92"
          width="92"
        />
          Лицевый счет кредитора #1000293091PZ
          
        </v-list-item-title>
        <v-list-item-subtitle>
          Дата открытия счета: 12.10.2021
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-card-text>
      <v-row align="left">
        <v-col
          class="display-3"
          cols="7"
        >
        Баланс: 173,600 Рублей 
        </v-col>
        <v-col cols="4">
        </v-col>
      </v-row>
    </v-card-text>
    
        <v-list-item-subtitle>
        </v-list-item-subtitle>
    <v-slider
      v-model="time"
      :max="6"
      :tick-labels="labels"
      class="mx-4"
      ticks
      label="Количество выданных ссуд при Вашем лимите:"
    >
          Количество выданных ссуд при Вашем лимите:</v-slider>



    <v-list class="transparent">

    <v-list-item>
      <v-list-item-icon>
        <v-icon>mdi-send</v-icon>
      </v-list-item-icon>
      <v-list-item-subtitle>Отправить запрос в службу технической поддержки</v-list-item-subtitle>
    </v-list-item>

    </v-list>

    <v-divider></v-divider>

  </v-card>




    </v-tab-item>
  </v-tabs>
  
</div>
  
</template>
<script>
  export default {
    data: () => ({
      dialog: '',
        singleSelect: false,
        labels: ['1', '2', '3', '4', '5', '6', '7'],
        time: 1,
        forecast: [
          { day: 'Tuesday', icon: 'mdi-white-balance-sunny', temp: '24\xB0/12\xB0' },
          { day: 'Wednesday', icon: 'mdi-white-balance-sunny', temp: '22\xB0/14\xB0' },
          { day: 'Thursday', icon: 'mdi-cloud', temp: '25\xB0/15\xB0' },
        ],
        name:"./../../assets/logo.png",
        selected: [],
        numbers: [ 1, 2, 3, 4, 5 ],
        headers: [
          {
            text: 'ФИО',
            value: 'ФИО',
          },
          { text: 'Рейтинг', value: 'Рейтинг' },
          { text: 'Департамент', value: 'Департамент' },
          { text: 'Компания', value: 'Компания' },
          { text: 'Никнейм', value: 'Никнейм' },
          { text: 'Стаж', value: 'Стаж' },
        ],
        headersCHIP: [
          {
            text: 'ФИО',
            value: 'ФИО',
          },
          { text: 'Сумма', value: 'Сумма' },
          { text: 'Компания', value: 'Компания' },
          { text: 'Остаток', value: 'Остаток' },
          { text: 'Срок', value: 'Срок' },
          { text: 'Никнейм', value: 'Никнейм' },
        ],
        desserts: [
          {
            ФИО: 'Абаканович Ефим Родионов',
            Рейтинг: 59,
            Компания: 'Тандер',
            Департамент: 'Департамент развития',
            Стаж: '3 года',
            Никнейм: 'abakanovich_er',
          },
          {
            ФИО: 'Гордич Воланд Артемович',
            Рейтинг: 80,
            Компания: 'ВТБ',
            Департамент: 'Департамент логистики',
            Стаж: '7 лет',
            Никнейм: 'gordich_va',
          },
          {
            ФИО: 'Полевая Антонина Михайловна',
            Рейтинг: 23,
            Компания: 'ВТБ',
            Департамент: 'Департамент продаж',
            Стаж: '8 месяцев',
            Никнейм: 'polevaya_am%',
          },
          {
            ФИО: 'Гладких Карина Аароновна',
            Рейтинг: 92,
            Компания: 'ВТБ',
            Департамент: 'Департамент маркетинга',
            Стаж: '10 лет',
            Никнейм: 'gladkikh_ka',
          },
        ],
        dessertsCHIP: [
          {
            ФИО: 'Дель Рэй Лана',
            Сумма: '180,000',
            Компания: 'Тандер',
            Остаток: '123,780',
            Срок: '1 год 6 месяцев',
            Ставка: '10,9%',
            Никнейм: 'abakanovich_er',
          },
          {
            ФИО: 'Леонидов Леонид Леонидович',
            Сумма: '90,000',
            Компания: 'ВТБ',
            Остаток: '11,090',
            Срок: '1 год 6 месяцев',
            Стаж: '14,9%',
            Никнейм: 'gordich_va',
          },
        ],
      items: [
        {
          color: '#1F7087',
          title: 'Алевтина Марковна Осипова',
          artist: 'Сумма займа:',
        },
        {
          color: '#952175',
          title: 'Виталий Викторович Попов',
          artist: 'Сумма займа:',
        },
      ],
    }),
  }
</script>