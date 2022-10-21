<template>
  <body style="height: 748px width: 679px">
    <div id="container">
      <div id="header" class="header"></div>
      <div class="Nsearch">
        <div class="search_inner">
          <div class="search_nav">
            <div class="search_box">
              <div class="search_box_inner">
                <span class="search_text_box">
                  <input
                    type="search"
                    name="search_query"
                    value
                    maxlength="100"
                    placeholder="버스번호, 정류장 검색"
                    title="검색어 입력"
                    class="search_text"
                  />
                </span>
                <span class="box_tool">
                  <button type="button" class="box_button2">
                    <span class="icon_delete">검색어 삭제</span>
                  </button>
                  <button type="submit" class="search_button">
                    <span class="icon_submit">검색</span>
                  </button>
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      sampleData: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
<style scoped>
#container {
  width: 679px;
  min-height: 748px;
}
#header {
  text-align: center;
  color: #fff;
}
.search_text {
  box-sizing: border-box;
  width: 100%;
  height: 42px;
  padding: 0 12px;
  border: 0;
  font-size: 17px;
  color: #000;
  font-weight: bold;
  line-height: 26px;
  background: none;
}
.search_text_box {
  display: table-cell;
  width: 100%;
  vertical-align: top;
}
.search_box_inner {
  display: table;
  width: 100%;
}
.Nsearch {
  position: relative;
  padding: 6px 6px 6px 6px;
  line-height: 14px;
  background-color: #00c73c;
}
.search_box {
  box-sizing: border-box;
  width: 100%;
  vertical-align: top;
  background-color: #fff;
}
.search_inner {
  display: table;
  width: 100%;
}
.search_nav {
  display: table-cell;
  width: 40px;
  vertical-align: top;
}
.search_nav_link {
  display: block;
  position: relative;
  width: 36px;
  height: 42px;
  margin-right: 6px;
}
.box_tool {
  overflow: hidden;
  display: table-cell;
  font-size: 0;
  text-align: right;
  white-space: nowrap;
  vertical-align: top;
}
.box_button2 {
  overflow: hidden;
  position: relative;
  height: 42px;
  margin: 0;
  padding: 0;
  border: 0;
  line-height: 42px;
  vertical-align: top;
  background: none;
  display: none;
}
.icon_delete {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: linear-gradient(transparent, transparent),
    url(https://ssl.pstatic.net/static/maps/m/sp_search.svg);
  background-size: 95px 91px;
  background-repeat: no-repeat;
  width: 18px;
  height: 18px;
  background-position: -34px -40px;
  margin: auto;
  color: transparent;
}
.search_button {
  display: inline-block;
  overflow: hidden;
  position: relative;
  height: 42px;
  margin: 0;
  padding: 0;
  border: 0;
  line-height: 42px;
  vertical-align: top;
  background: none;
}
.icon_submit {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: linear-gradient(transparent, transparent),
    url(https://ssl.pstatic.net/static/maps/m/sp_search.svg);
  background-size: 95px 91px;
  background-repeat: no-repeat;
  width: 18px;
  height: 18px;
  background-position: -6px -68px;
  margin: auto;
  color: transparent;
}
</style>
