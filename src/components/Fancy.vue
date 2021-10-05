<template>
  <div class="container">
    <div class="input">
      <textarea
        name="txt"
        id="txt"
        v-model="msg"
        placeholder="Please enter keywords..."
      ></textarea>
    </div>
    <span class="tips"
      >tips: 点击对应字体即可复制到剪切板 可粘贴到微信QQ或其它输入框
      仅英文</span
    >
    <div class="output">
      <ul class="list">
        <li @click="copyText(italic)">
          {{ italic }}
        </li>
        <li @click="copyText(bold)">{{ bold }}</li>
        <li @click="copyText(boldItalic)">
          {{ boldItalic }}
        </li>
        <li @click="copyText(normal)">
          {{ normal }}
        </li>
        <!-- <hr> -->
        <li @click="copyText(sansSerifItalic)">
          {{ sansSerifItalic }}
        </li>
        <li @click="copyText(sansSerifBold)">
          {{ sansSerifBold }}
        </li>
        <li @click="copyText(sansSerifBoldItalic)">
          {{ sansSerifBoldItalic }}
        </li>
        <li @click="copyText(sanSerifNormal)">
          {{ sansSerifNormal }}
        </li>
        <!-- <hr> -->
        <li @click="copyText(square)">
          {{ square }}
        </li>
        <li @click="copyText(circle)">
          {{ circle }}
        </li>
        <li @click="copyText(monoSpace)">
          {{ monoSpace }}
        </li>
        <li @click="copyText(doubleStruck)">
          {{ doubleStruck }}
        </li>
        <!-- <hr> -->
        <li @click="copyText(scriptNormal)">
          {{ scriptNormal }}
        </li>
        <li @click="copyText(scriptBold)">
          {{ scriptBold }}
        </li>
        <li @click="copyText(frakturNormal)">
          {{ frakturNormal }}
        </li>
        <li @click="copyText(frakturBold)">
          {{ frakturBold }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
import { doubleStruck, monoSpace, serif } from "weird-fonts"
import { square, circle, script} from "weird-fonts"
import { sansSerif, fraktur } from "weird-fonts"
import Toast from '../plugin/Toast'

export default {
  data() {    
    return {
      msg: 'I love three things in the world, sun moon and you, sun for morning, moon for night, and you forever.',
    }
  },
  computed: {
    normal:{
      get(){
        return serif(this.msg, { fontStyle: ""});
      }
    },
    italic:{
      get(){
        return serif(this.msg, { fontStyle: "italic" });
      }
    },
    bold:{
      get(){
        return serif(this.msg, { fontStyle: "bold" });
      }
    },
    boldItalic:{
      get(){
        return serif(this.msg, { fontStyle: "bold-italic" });
      }
    },
    square:{
      get(){
        return square(this.msg, { fontStyle: "" });
      }
    },
    sansSerifItalic:{
      get(){
        return sansSerif(this.msg, { fontStyle: "italic" });
      }
    },
    sansSerifBold:{
      get(){
        return sansSerif(this.msg, { fontStyle: "bold" });
      }
    },
    sansSerifBoldItalic:{
      get(){
        return sansSerif(this.msg, { fontStyle: "bold-italic" });
      }
    },
    sansSerifNormal:{
      get(){
        return sansSerif(this.msg, { fontStyle: ""});
      }
    },
    monoSpace:{
      get(){
        return monoSpace(this.msg, { fontStyle: ""});
      }
    },
    circle:{
      get(){
        return circle(this.msg, { fontStyle: ""});
      }
    },
    doubleStruck:{
      get(){
        return doubleStruck(this.msg, { fontStyle: ""});
      }
    },
    scriptNormal:{
      get(){
        return script(this.msg, { fontStyle: ""});
      }
    },
    scriptBold:{
      get(){
        return script(this.msg, { fontStyle: "bold"});
      }
    },
    frakturNormal:{
      get(){
        return fraktur(this.msg, { fontStyle: ""});
      }
    },
    frakturBold:{
      get(){
        return fraktur(this.msg, { fontStyle: "bold"});
      }
    },
  },

  methods: {
    copyText(text){
      var textareaEl = document.createElement('textarea');
      textareaEl.setAttribute('readonly', 'readonly'); 
      textareaEl.value = text;
      document.body.appendChild(textareaEl);
      textareaEl.select();
      var res = document.execCommand('copy');
      document.body.removeChild(textareaEl);
      console.log("复制成功");
      this.icCopy();
      return res;
    },
    icCopy() {
      try {
          // Now that we've selected the anchor text, execute the copy command
          var msg = '复制成功' ;
          var type =  'success';
          Toast.init();
          Toast.show(msg, type, null);
          setTimeout(function () {
              Toast.hide();
          }, 10000);
        } catch (err) {
          Toast.init();
          Toast.show('Sorry, unable to copy', 'error', null);
          setTimeout(function () {
              Toast.hide();
          }, 10000);
      }
    }
    
  }
}
</script>
<style scoped>
.container {
  width: 100%;
  max-width: 860px;
  margin: 1.25em auto;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.input {
  width: 100%;
  display: flex;
}
#txt {
  margin: 10px auto;
  height: 30px;
  width: 70%;
  padding: 8px;
  border: 1px solid #eee;
}
.output {
  width: 100%;
  display: flex;
  text-align: left;
  flex-direction: column;
}
ul,
li {
  width: 90%;
  line-height: 1.5;
  font-size: 18px;
  word-wrap: break-word;
  margin: auto;
}
li {
  text-align: left;
  list-style-position: inside;
  margin: 0.5em auto;
}
.tips {
  font-size: 13px;
  color: #999;
  text-align: center;
}
.hover{
  background: cornflowerblue;
}
</style>