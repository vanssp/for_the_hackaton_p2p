<template>
    <v-container>
      <v-row>
        <v-col>

          <v-card
          elevation="0"
          >
            <v-card-title class="text-h5">
               Список доступных кредитных предложений:
            </v-card-title>
          </v-card>
        </v-col>
      </v-row>
      <v-row dense>
        <v-col cols="12">
          <v-card
          >
            <v-card-title class="text-h5">
               Сергей Сергеевич Городовой
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        />
            </v-card-title>
            
            <v-card-subtitle>Лимит допустимого займа: 140,000
            </v-card-subtitle>
            <v-card-actions>
              <v-btn>
          Подробные условия кредитования
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="12">
          <v-card
          >
            <v-card-title class="text-h5">
               Дмитрий Сергеевич Ломовой
        <v-img
          :src="require('../assets/mit.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        />
            </v-card-title>
            <v-card-subtitle>Лимит допустимого займа: 40,000
            </v-card-subtitle>
            <v-card-actions>
<div class="text-center">
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          v-bind="attrs"
          v-on="on"
        >
          Подробные условия кредитования
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="headline grey lighten-2">
          Информация по предложению
        </v-card-title>


        <v-divider></v-divider>

<v-container fluid>
    <v-row>
      <v-col cols="4">
        <v-subheader>Максимальный лимит займа</v-subheader>
      </v-col>
      <v-col cols="8">
        <v-text-field
          label="Руб"
          value="140,000"
          prefix=""
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4">
        <v-subheader>Ежемесячный платеж</v-subheader>
      </v-col>
      <v-col cols="8">
        <v-text-field
          label="Руб"
          value="10,000"
          prefix=""
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4">
        <v-subheader>Процент</v-subheader>
      </v-col>
      <v-col cols="8">
        <v-text-field
          label="%"
          value="10.0"
          prefix=""
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4">
        <v-subheader>Срок займа</v-subheader>
      </v-col>
      <v-col cols="8">
        <v-text-field
          label="Месяцев"
          value="14"
          prefix=""
        ></v-text-field>
      </v-col>
    </v-row>
  </v-container>
      </v-card>
    </v-dialog>
  </div>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="12">
          <v-card
          >
            <v-card-title class="text-h5">
               Кирилл Сергеевич Иванников
        <v-img
          :src="require('../assets/vtb.png')"
          class="my-3"
          contain
          height="25"
          width="25"
        />
            </v-card-title>
            <v-card-subtitle>Лимит допустимого займа: 100,000
            </v-card-subtitle>
            <v-card-actions>
              <v-btn>
          Подробные условия кредитования
                
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

       
      </v-row>
    </v-container>
</template>
<script>
  export default {
    data: () => ({
      dialog: '',
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