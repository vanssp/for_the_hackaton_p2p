<template>
  <v-app>
  <div>

    <v-app-bar
      color="#006699"
      dense
      dark
      height=79x
    >
      <v-btn icon>
        <v-icon
          dark
          right
        >
          mdi-checkbox-marked-circle
        </v-icon>
      </v-btn>

      <v-toolbar-title>P2P для корпоративного сектора</v-toolbar-title>

      <v-spacer></v-spacer>


      <span v-if="showOn">
      <v-toolbar-title>Иванов Иван Иванович (кредитор)</v-toolbar-title>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          

          <v-btn
            v-bind="attrs"
            v-on="on"
            color="#336699"
            @click="goOut"
      >
        <v-icon
          left
        >
          mdi-logout
        </v-icon>Выход
      </v-btn>
        </template>


        
      </v-menu>
      </span>

      <span v-if="showAdmin">
      <v-toolbar-title>Администратор</v-toolbar-title>
      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          

          <v-btn
            v-bind="attrs"
            v-on="on"
            color="#336699"
            @click="goOut"
      >
        <v-icon
          left
        >
          mdi-logout
        </v-icon>Выход
      </v-btn>
        </template>
      </v-menu>
      </span>

      <span v-if="showCreditable">
      <v-toolbar-title>Петров Виктор Викторович (Заемщик)</v-toolbar-title>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          

          <v-btn
            v-bind="attrs"
            v-on="on"
            color="#336699"
            @click="goOut"
      >
        <v-icon
          left
        >
          mdi-logout
        </v-icon>Выход
      </v-btn>
        </template>
      </v-menu>
      </span>

      <span v-if="loginShow">
      <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="red lighten-2"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Войти
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="headline grey lighten-2">
          Авторизация
        </v-card-title>
<v-form
      ref="form"
      v-model="form"
      class="pa-4 pt-6"
    >
      
      <v-text-field
        ref="log"
        v-model="email"
        filled
        color="dark"
        label="Логин"
        type="email"
      ></v-text-field>
      <v-text-field
        ref="pass"
        v-model="password"
        filled
        color="dark"
        counter="8"
        label="Пароль"
        style="min-height: 96px"
        type="password"
      ></v-text-field>
      <v-btn
        @click="go"
      >
          Вход
      </v-btn>
    </v-form>
      </v-card>
    </v-dialog>
  </div>
</span>
    </v-app-bar>
    <span v-if="showOn">
      <creditable/>
    </span>   


<span v-if="showAdmin">
  <adminpanel/>
</span>
    <span v-if="showCreditable">
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
          mdi-charity
        </v-icon>
      Список кредитных продуктов
      </v-tab>
      <v-tab>
        <v-icon left>
          mdi-cash-100
        </v-icon>
      Баланс лицевого счета
      </v-tab>

      <v-tab-item>



    <v-card-title>Ваш рейтинг заемщика</v-card-title>

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

      <div class="my-4 subtitle-1">Петров Виктор Викторович
      </div>
      <div>Через 6 дней Ваши данные будут обновлены.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>


    <v-card-title>Лицевой счет:</v-card-title>
      <v-row no-gutters>
      <v-col
        cols="2"
      >
        <v-card
          class="pa-1"
          tile
          elevation="0"
        >
         
    <v-card-text> Баланс
      <v-chip-group
        active-class="grey accent-4 white--text"
        column
      >
        <v-chip>98,780 Рублей</v-chip>
      </v-chip-group>
    </v-card-text>

        </v-card>
      </v-col>
      <v-col
       cols="2"
      >
        <v-card
          class="pa-1"
          tile
          elevation="0"
        >
    <v-card-text> Размер ставки
      <v-chip-group
        active-class="grey accent-4 white--text"
        column
      >
        <v-chip>10,9%</v-chip>
      </v-chip-group>
    </v-card-text>
        </v-card>

      </v-col>
      <v-col
       cols="2"
      >
        <v-card
          class="pa-1"
          tile
          elevation="0"
        >
    <v-card-text> Начисление пени
      <v-chip-group
        active-class="grey accent-4 white--text"
        column
      >
        <v-chip>0,0 Рублей</v-chip>
      </v-chip-group>
    </v-card-text>
        </v-card>

      </v-col>
      <v-col
       cols="2"
      >
        <v-card
          class="pa-1"
          tile
          elevation="0"
        >
    <v-card-text> Дата платежа
      <v-chip-group
        active-class="grey accent-4 white--text"
        column
      >
        <v-chip>21 Июня 2021</v-chip>
      </v-chip-group>
    </v-card-text>
        </v-card>

      </v-col>
    </v-row>
    
      <v-row no-gutters
      >
          <v-btn
          rounded
          color="red lighten-2"
      >Частичное погашение
      </v-btn>
          <v-btn
          rounded
          color="red lighten-2"
      >Полное погашение
      </v-btn>
          <v-btn
          rounded
          color="red lighten-2"
      >Детальная информация
      </v-btn>
    </v-row>



      </v-tab-item>
      <v-tab-item>
        
 
      <login/>
        

      </v-tab-item>
      <v-tab-item>
        <v-container>
    <v-row justify="space-around">
      <v-card width="500"
    color="amber"
    dark
    class="mx-auto my-12"
      
      >
        
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >

            <v-toolbar-title class="title white--text pl-0">
              Остаток на счете:
            </v-toolbar-title>

            <v-spacer></v-spacer>

            <v-btn
              color="white"
              icon
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-app-bar>

          <v-card-title class="white--text mt-8">
            <p class="ml-9">
              123,560 Рублей
            </p>
          </v-card-title>

      </v-card>
    </v-row>
  </v-container>
        

      </v-tab-item>
    </v-tabs>
</span>

  </div>
  </v-app>
</template>

<script>
import Login from './components/Login'
import Creditable from './components/Creditable'
import Admin from './components/Admin'

export default {
  name: 'App',
  components: {
    login: Login,
    creditable: Creditable,
    adminpanel: Admin
  },
  methods: {
    go() {
        console.log()
        if (this.$refs.log.$refs.input._value == "Ivanov" || this.$refs.log.$refs.input._value == "ivanov") {
          this.showOn = true; 
          this.showCreditable = false;
          this.loginShow = false;
          this.showAdmin = false;
        } else if (this.$refs.log.$refs.input._value == "Petrov" || this.$refs.log.$refs.input._value == "petrov") {
          this.showOn = false; 
          this.loginShow = false;
          this.showCreditable = true;
          this.showAdmin = false;
        } else if (this.$refs.log.$refs.input._value == "Admin" || this.$refs.log.$refs.input._value == "admin") {
          this.showOn = false; 
          this.loginShow = false;
          this.showCreditable = false;
          this.showAdmin = true;
        }
    },
    goOut() {
        this.showOn = false;
        this.loginShow = true;
        this.showCreditable = false;
    }
  },
  data () {
      return {
        selection: '',
        showAdmin: false,
        showOn: false,
        showCreditable: false,
        dialog: false,
        loginShow: true,
        agreement: false,
        email: undefined,
        form: false,
        isLoading: false,
        password: undefined,
      }
    },
};
</script>       