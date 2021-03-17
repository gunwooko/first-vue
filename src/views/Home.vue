<template>
<!-- Vue 파일은 컴포넌트 템플릿을 정의하는 template 파트, 스크립트를 작성하는 script 파트, 그리고 스타일링 정보를 작성하는 style 파트로 나누어져 있다. -->
  <div>
      <!-- 중괄호를 두번 사용해서 JS 데이터를 보여줄 수 있다. Mustache bracket-->
    <h1>Welcome to {{title2}}!</h1>
    <!-- v-model 를 사용해서 input 값을 가져올 수 있다. 또한 양방향 데이터 바인딩이기에 data()에 정의된 데이터 변경이 가능하다.  -->
    <input type="text" v-model="input1" />
    <!-- @click 을 이용해서 클릭 이벤트를 헨들링 할 수 있다. -->
    <!-- v-on의 약어 => v-on:click을 @click으로 사용 가능하다. -->
    <button type="button" @click="getData">Get</button>
    <button type="button" @click="setData">Set</button>
    <!-- @change 를 이용해서 값의 변화를 확인하고 설정할 수 있다. -->
    <select class="form-control" v-model="region" @change="changeRegion">
        <!-- v-for 를 이용해서 반복문을 돌릴 수 있다. 데이터 형식이 배열로 주어졌을 때 -->
        <!-- :key는 v-bind:key의 약어이다 -->
      <option :key="i" :value="d.v" v-for="(d,i) in options">{{d.t}}</option>
    </select>
    <div>
        <!-- v-if 를 이용해 조건부 렌더링으 할 수 있다. -->
        <h3 v-if="awesome"> Vue is awesome! </h3>
        <h1 v-else>Oh no 😢</h1>
    </div>
    <!-- v-show 를 이용해 display css 속성을 none 처럼 할 수 있다. <엘리먼트는 렌더링이 된다.> -->
    <table class="table table-bordered" v-show="tableShow">
      <tr :key="index" v-for="(data,index) in options">
        <td>{{data.v}}</td>
        <td>{{data.t}}</td>
      </tr>
    </table>
  </div>
</template>
<script>
export default {
    // data 메소드를 통해 다루고 싶은 데이터를 정의하고, 다룰 수 있게 된다. 
    // 이곳에서 데이터를 정의하고, template에 mustache bracket을 이용해 데이터를 바인딩 할 수 있다. 
    // 또한 데이터를 가지고 오고 싶다면(ex. input, select, etc), v-model를 사용해서 아래의 변수에 할당할 수 있다. 
    // 위처럼 양방향으로 데이터 바인딩이 가능하게 된다. 
  data() {
    return {
      title: "뷰 연습",
      title2: "Seoul",
      input1: "abcd",
      options: [
        { v: "S", t: "Seoul" },
        { v: "J", t: "Jeju" },
        { v: "B", t: "Busan" },
      ],
      region: "B",
      tableShow: false,
      awesome: false,
    };
  },
  // 만일 데이터에 조금이라도 변경이 일어나면 왓치 안에 정의된 해당 함수가 작용된다. 
  // 왓치는 데이터 변경을 알아서 캐치해준다. (모니터링 기능) 특정 데이터를 항상 주시하고 있다가, 변경이 일어나면 그 데이터를 캐치해서 사용할 수 있다.
  // 주로 사용자로부터의 이벤트가 아닌 프로그램 상에서 어떠한 특정 데이터가 변경하는 것을 확인하고 싶을 때 사용하면 좋다.  
  watch: {
      // 왓치에선 데이터 명을 그대로 가지고와서 함수형태로 작성해서 사용한다. 
    input1() {
      console.log(this.input1);
    },
    title() {},
  },
  // Vue에서는 모든 메서드를 이곳에 정의를 한다. 
  // 데이터 컨트롤에 관련된 모든 것을 이곳에서 정의한다. 
  methods: {
    getData() {
      alert(this.input1);
    },
    setData() {
      this.input1 = "12345";
    },
    changeRegion() {
      alert(this.region);
    },
  },
  // Vue 인스턴스의 라이프 사이클
  // 만일 처음 화면 렌더링이 되기 전에 DB와 같은 곳에서 데이터를 가져와 뿌려야 한다고 한다면 이곳에서 적용하면 된다. 
  beforeCreate() {
    console.log("beforeCreate");
  },
  created() {
    console.log("created");
  },
  beforeMount() {
    console.log("beforeMount");
  },
  // 화면에 실제로 html이 로딩이 되었을 때
  mounted() {
    console.log("mounted");
  },
  // 데이터가 변경될 때, 데이터가 변경하기 전에 무언가를, 함수를 적용하고 싶을 때 이곳에 정의하면 된다. 
  beforeUpdate() {
    console.log("beforeUpdate");
  },
  updated() {
    console.log("updated");
  },
  beforeDestroy() {
    console.log("beforeDestroy");
  },
  destroyed() {
    console.log("beforeDestroy");
  },
};
</script>