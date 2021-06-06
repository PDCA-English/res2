<template>
<div id="app">
  <Logo />
  <div class="info">
    <div class="infoHead">
      <button>&lt;</button>
      <h1>仙人</h1>
    </div>
    <img src="https://coachtech-matter.s3-ap-northeast-1.amazonaws.com/image/sushi.jpg" alt="">
    <p>#東京 ＃寿司</p>
    <p>料理長厳選の食材から作る寿司を用いたコースをぜひお楽しみください。食材・味・価格、お客様の満足度を徹底的に追及したお店です。特別な日のお食事、ビジネス接待まで気軽に使用することができます。</p>
  </div>
  <div class="reservation">
    <h2>予約</h2>
    <p class="explanation">ご予約の人数を入力ください。</p>
    <select name="people" v-model="people">
      <option value="1">1人</option>
      <option value="2">2人</option>
      <option value="3">3人</option>
      <option value="4">4人</option>
      <option value="5">5人</option>
      <option value="6">6人</option>
      <option value="7">7人</option>
      <option value="8">8人</option>
      <option value="9">9人</option>
      <option value="10">10人</option>
    </select>
      <table>
        <tr>
          <th></th>
          <th v-for="date in thisWeek" v-bind:key="date">{{date[0]}}月{{date[1]}}日（{{date[2]}}）</th>
        </tr>
        <tr>
          <td>10:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[0]}}</td>
        </tr>
        <tr>
          <td>10:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[1]}}</td>
        </tr>
        <tr>
          <td>11:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[2]}}</td>
        </tr>
        <tr>
          <td>11:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[3]}}</td>
        </tr>
        <tr>
          <td>12:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[4]}}</td>
        </tr>
        <tr>
          <td>12:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[5]}}</td>
        </tr>
        <tr>
          <td>13:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[6]}}</td>
        </tr>
        <tr>
          <td>13:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[7]}}</td>
        </tr>
        <tr>
          <td>14:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[8]}}</td>
        </tr>
        <tr>
          <td>14:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[9]}}</td>
        </tr>
        <tr>
          <td>15:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[10]}}</td>
        </tr>
        <tr>
          <td>15:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[11]}}</td>
        </tr>
        <tr>
          <td>16:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[12]}}</td>
        </tr>
        <tr>
          <td>16:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[13]}}</td>
        </tr>
        <tr>
          <td>17:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[14]}}</td>
        </tr>
        <tr>
          <td>17:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[15]}}</td>
        </tr>
        <tr>
          <td>18:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[16]}}</td>
        </tr>
        <tr>
          <td>18:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[17]}}</td>
        </tr>
        <tr>
          <td>19:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[18]}}</td>
        </tr>
        <tr>
          <td>19:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[19]}}</td>
        </tr>
        <tr>
          <td>20:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[20]}}</td>
        </tr>
        <tr>
          <td>20:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[21]}}</td>
        </tr>
        <tr>
          <td>21:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[22]}}</td>
        </tr>
        <tr>
          <td>21:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[23]}}</td>
        </tr>
        <tr>
          <td>22:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[24]}}</td>
        </tr>
        <tr>
          <td>22:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[25]}}</td>
        </tr>
        <tr>
          <td>23:00</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[26]}}</td>
        </tr>
        <tr>
          <td>23:30</td>
          <td v-for="availability in dateList" v-bind:key="availability">{{availability[27]}}</td>
        </tr>
      </table>
    
    <div class="summary">
      <table>
        <tr>
          <th>Shop</th>
          <td>仙人</td>
        </tr>
        <tr>
          <th>Date</th>
          <td>{{date}}</td>
        </tr>
        <tr>
          <th>Time</th>
          <td>{{time}}</td>
        </tr>
        <tr>
          <th>Number</th>
          <td>{{people}}</td>
        </tr>
      </table>
    </div>
  <button>予約する</button>
  </div>

</div>
</template>

<script>
import Logo from "../components/Logo";
export default {
 components: {
   Logo
 },
 data() {
   return {
     date: "",
     time: "",
     people: "",
     thisWeek: [],
     timeList: [
       "10:00",
       "10:30",
       "11:00",
       "11:30",
       "12:00",
       "12:30",
       "13:00",
       "13:30",
       "14:00",
       "14:30",
       "15:00",
       "15:30",
       "16:00",
       "16:30",
       "17:00",
       "17:30",
       "18:00",
       "18:30",
       "19:00",
       "19:30",
       "20:00",
       "20:30",
       "21:00",
       "21:30",
       "22:00",
       "22:30",
     ],
     dateList: [
       [
         "a",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
       ],
       [
         "b",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
       ],
       [
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
       ],
       [
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
       ],
       [
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
       ],
       [
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
       ],
       [
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
         "◯",
       ],
     ],
   }
 },
 async created() {
   for(let i = 0; i < 7; i++) {
     if (i === 0) {
       var today = new Date();
       this.thisWeek = new Array();
     }
     var dateAndDay = [];

     var dateList = ["日","月","火","水","木","金","土"];
     var day = dateList[today.getDay()];

     dateAndDay.push(today.getMonth()+1);
     dateAndDay.push(today.getDate());
     dateAndDay.push(day);
    //  console.log(dateAndDay)

     today.setDate(today.getDate() + 1);
    //  console.log("today",today)

     this.thisWeek.push(dateAndDay);
     dateAndDay = [];
     console.log(this.thisWeek)
   }
 },
 methods: {
   alert() {
     alert("hey");
   }
}
};
</script>

<style scoped>
#app {
  display: flex;
}

.info {
  position: relative;
  padding: 150px 100px; 
  width: 50%;
}

.infoHead {
  display: flex;
  margin-bottom: 30px;
}

img {
  width: 100%;
}

.reservation {
  width: 50%;
  background-color: #305CFF;
  border-radius: 5px;
  margin: 155px 50px 30px 50px;
  height: 50%;
  padding-top: 20px;
  color: #fff;
  position: relative;
  box-shadow: 2px 2px 4px gray;

}

.reservation button {
  position: relative;
  bottom: 0;
  text-align: center;
  width: 100%;
  height: 60px;
  background-color: #0238FF;
  padding: 10px 0;
  margin: 20px 0 0 0;
  border-radius: 0 0 5px 5px;
  color: #fff;
  font-size: 15px;
}

button {
  background-color: #fff;
  border-radius: 5px;
  border: none;
  width: 45px;
  height: 45px;
  font-size: 30px;
  margin-right: 20px;
  box-shadow: 2px 2px 4px gray;
}

h1 {
  margin: 0;
}

input, select {
  display: block;
  height: 40px;
  margin-bottom: 15px;
  border-radius: 5px;
  border: none;
  padding-left: 10px;
}

select {
  width: 40vw;
}

h2, input, select {
  margin-right: 30px;
  margin-left: 30px;
}

.summary {
  background-color: #4D7EFF;
  margin-left: 30px;
  border-radius: 5px;
  padding: 15px;
  width: 35vw;
  text-align: left;
  margin-top: 20px;

}

th {
  width: 10vw;
}

.explanation {
  text-align: left;
  padding-left: 32px;
  margin-bottom: 4px;
}
</style>