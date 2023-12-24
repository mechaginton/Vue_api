<!-- <template>
    <main>
      <div>
        <h2>“s“¹•{Œ§</h2>
        <div class='input_area'>
          <input type='radio' id='hokkaido' value='–kŠC“¹' v-model='value' @change='getPrefectures()' />
          <label for='hokkaido'>–kŠC“¹</label>
          <input type='radio' id='touhoku' value='“Œ–k' v-model='value' @change='getPrefectures()' />
          <label for='touhoku'>“Œ–k</label>
          <input type='radio' id='kantou' value='ŠÖ“Œ' v-model='value' @change='getPrefectures()' />
          <label for='kantou'>ŠÖ“Œ</label>
          <input type='radio' id='chubu' value='’†•”' v-model='value' @change='getPrefectures()' />
          <label for='chubu'>’†•”</label>
          <input type='radio' id='kinki' value='‹ß‹E' v-model='value' @change='getPrefectures()' />
          <label for='kinki'>‹ß‹E</label>
          <input type='radio' id='chugoku' value='’†‘' v-model='value' @change='getPrefectures()' />
          <label for='chugoku'>’†‘</label>
          <input type='radio' id='shikoku' value='l‘' v-model='value' @change='getPrefectures()' />
          <label for='shikoku'>l‘</label>
          <input
            type='radio'
            id='kyushu_okinawa'
            value='‹ãB'
            v-model='value'
            @change='getPrefectures()'
          />
          <label for='kyushu_okinawa'>‹ãB‰«“ê</label>
        </div>
        <div class='result_area'>
          <ul>
            <li v-for='item in result.response.prefecture' :key='item'>{{ item }}</li>
          </ul>
        </div>
      </div>
    </main>
  </template>
  
  <script>
  export default {
    data () {
      return {
        value: '',
        result: {
          response: {
            prefecture: []
          }
        },
        changed: false
      }
    },
    created () {
      this.axios.get('http://geoapi.heartrails.com/api/json', {
        params: {
          method: 'getPrefectures',
          area: '–kŠC“¹'
        }
      })
        .then(response => {
          this.result = response.data
        })
        .catch(err => {
          console.error(err)
        })
    },
    methods: {
      getPrefectures: function () {
        this.axios.get('http://geoapi.heartrails.com/api/json', {
          params: {
            method: 'getPrefectures',
            area: this.value
          }
        })
          .then(response => {
            this.result = response.data
          })
          .catch(err => {
            console.error(err)
          })
      }
    }
  }
  </script>
  
  <style scoped>
  main {
    height: calc(100vh - 152px);
    padding: 3% 0;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  h2 {
    margin-bottom: 1.5em;
  }
  .input_area {
    margin-bottom: 15%;
  }
  .result_area {
    min-height: 300px;
  }
  ul {
    padding-left: 0;
  }
  ul li {
    list-style: none;
  }
  </style>
   -->