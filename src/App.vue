<template>
  <div class="container">
    <div class="mahoa">
      <div class="header">Mã hóa</div>
      <div class="content">
        <div class="c1">
          <div>Bản rõ</div>
          <div class="input">
            <textarea
              type="text"
              style="
                min-height: 100px;
                max-height: 100px;
                min-width: 170px;
                max-width: 170px;
              "
              v-model="txtMaHoa"
            />
          </div>
          <div>
            <button>File</button>
          </div>
        </div>
        <div class="func" @click="maHoa">
          <button>Mã hóa</button>
        </div>
        <div class="c2">
          <div>Bản mã</div>
          <div class="input">
            <textarea
              type="text"
              v-model="txtKQMaHoa"
              style="
                min-height: 100px;
                max-height: 100px;
                min-width: 170px;
                max-width: 170px;
              "
            />
          </div>
          <div style="display: flex; flex-direction: column">
            <button>Chuyển</button>
            <button style="margin-top: 20px">Lưu</button>
          </div>
        </div>
      </div>
    </div>
    <div class="giaima">
      <div class="header">Giải mã</div>
      <div class="content">
        <div class="c1">
          <div>Bản mã</div>
          <div class="input">
            <textarea
              type="text"
              style="
                min-height: 100px;
                max-height: 100px;
                min-width: 170px;
                max-width: 170px;
              "
              v-model="txtGiaiMa"
            />
          </div>
          <div>
            <button>File</button>
          </div>
        </div>
        <div class="func" @click="giaiMa">
          <button>Giải mã</button>
        </div>
        <div class="c2">
          <div>Bản rõ</div>
          <div class="input">
            <textarea
              type="text"
              v-model="txtKQGiaiMa"
              style="
                min-height: 100px;
                max-height: 100px;
                min-width: 170px;
                max-width: 170px;
              "
            />
          </div>
          <div>
            <button>Lưu</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      txtMaHoa: "",
      txtKQMaHoa: "",
      txtGiaiMa: "",
      txtKQGiaiMa: "",
    };
  },
  methods: {
    maHoa() {
      this.txtMaHoa = "tesst";
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  width: 100%;
}

.container {
  display: flex;
}

.mahoa {
  border-right: 1px solid #bbb;
  height: 100%;
  width: 50%;
}

.giaima {
  width: 50%;
  height: 100%;
}

.header {
  padding: 60px 0;
}

.c1,
.c2 {
  display: flex;
  justify-content: space-evenly;
}

textarea:focus {
  border: 1px solid #00dfa2;
  outline: none !important;
  box-shadow: 0 0 10px #719ece;
  padding-left: 8px;
}

.func {
  padding: 20px 0;
}

button {
  color: black;
  background-color: #30a2ff;
  border: 1px solid #bbb;
  padding: 4px 8px;
}
</style>
