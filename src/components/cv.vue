<template>
  <v-app>
    <v-container id="wrapper">
      <div class='top'>
        <v-row no-gutters>
          <v-col lg='4' style="display: flex; justify-content: center; align-items: center">
            <div class="image-border">
              <input type="image" src="ava.png" style="width: 135px; height: 135px; border-radius: 50%"/>
            </div>
          </v-col>
          <v-col lg='8'>
            <div class="info">
            <input type="text" class="name"/>
            <v-row no-gutters>
              <v-col lg='5'>
                <div>
                  <i class="fas fa-calendar-alt"></i>
                  <input type="text" id="birthday" class="info_item">
                </div>
                <div>
                  <i class="fas fa-phone-alt"></i>
                  <input type="text" id="phone" class="info_item">
                </div>
                <div>
                  <i class="fas fa-map-marker-alt"></i>
                  <input type="text" id="location" class="info_item">
                </div>
              </v-col>
              <v-col lg='7'>
                <div>
                  <i class="fas fa-user-alt"></i>
                  <input type="text" id="gender" class="info_item">
                </div>
                <div>
                  <i class="fas fa-envelope"></i>
                  <input type="text" id="mail" class="info_item">
                </div>
                <div>
                  <i class="fas fa-info"></i>
                  <input type="text" id="site" class="info_item">
                </div>
              </v-col>
            </v-row>
          </div></v-col>
        </v-row>  
      </div>
      <div class="line"></div>
      <div class='bottom'>
        <v-container>
          <v-row>
            <v-col lg='6'>
              <div class="left_banner">
                <div class="left_contain">
                  <div class="title">EDUCATION</div>
                  <div class="subline"></div>
                  <Education />
                  <Education />
                </div>
                <div class="left_contain">
                  <div class="title">EXPERIENCE</div>
                  <div class="subline"></div>
                  <Exp />
                  <Exp />
                </div>
                <div class="left_contain">
                  <div class="title">ACTIVITIES AND AWARD</div>
                  <div class="subline"></div>
                  <Act />
                </div>
                <div class="left_contain">
                  <div class="title">CERTIFICATIONS</div>
                  <div class="subline"></div>
                  <Cer />
                </div>
              </div>
            </v-col>
            <v-col lg='6'>
              <div class="right_banner">
                <div class="right_contain">
                  <div class="title">OBJECTIVE</div>
                  <div class="subline"></div>
                  <div><textarea class="obj" rows="3">With logical thinking skills and a creative mindset, I want to be come one of the key members who bring an effective IT solution to the customers. At the same time, I want to improve my knowledge through your professional working environment.</textarea></div>
                </div>
                <div class="right_contain">
                  <div class="title">SKILL</div>
                  <div class="subline"></div>
                  <Skill />
                  <Skill />
                  <Skill />
                  <Skill />
                  <Skill />
                  <Skill />
                </div>
                <div class="right_contain">
                  <div class="title">FAVORITE</div>
                  <div class="subline"></div>
                  <fav />
                  <fav />
                  <fav />
                </div>
                <div class="right_contain">
                  <div class="title">ADDITIONAL INFORMATION</div>
                  <div class="subline"></div>
                  <div><textarea class="addinfo" rows="2">Tìm hiểu thêm thông tin qua các link bên trên</textarea></div>
                </div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
      </v-container>
  </v-app>
</template>
<script>
import Education from './Education.vue'
import Exp from './Experience.vue'
import Act from './Activity.vue'
import Cer from './Certi.vue'
import Skill from './Skill.vue'
import fav from './Favorite.vue'
export default {
  name: 'cv',
  components: {
    Education,
    Exp,
    Act,
    Cer,
    Skill,
    fav,
  }
}
</script>

<style>
  .app {
    width: 100%;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  input {
    max-width: 100%;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  input:focus {
    outline: none;
    box-shadow: 0 0 10px aqua;
  }
  textarea:focus{
    outline: none;
    box-shadow: 0 0 10px aqua;
  }
  #wrapper {
    width: 70%;
    height: 100%;
    margin-bottom: 10px;
    padding: 0;
    border: 1px solid coral;
    box-shadow: 10px 10px lightsalmon;
  }
  .image-border {
    width: 150px;
    height: 150px;
    display: flex;
    justify-items: center;
    text-align: center;
    border-radius: 50%;
    background-color: coral;
  }
  .image-border > input[type="image"] {
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    margin: auto;
  }
  .info{
    margin-left: 30px;
  }
  .name {
    font-weight: bold;
    font-size: 28px;
    color: coral;
  }
  .top{
    background-color: antiquewhite; 
    margin-bottom: 0;
    padding-top: 20px;
    padding-bottom: 20px;
  }
  i {
    width: 12px;
    margin-right: 5px;
  }

  .info_item {
    margin-left: 5px;
    display: inline-block;
    margin-top: 6px;
    font-size: 15px;
  }
  .line {
    margin: 0 0 20px 0;
    border: 10px solid lightsalmon;
  }
  
  .subline {
    margin-bottom: 20px;
    width: 70px;
    border: 3px solid lightsalmon;
  }
  .left_contain,
  .right_contain {
    width: 100%;
    max-height: 50%;
    margin-bottom: 40px;
  }
  .ver_line {
    line-height: 100%;
    border-left: 3px solid lightsalmon;
    margin-right: 15px;
    margin-left: 8px;
  }
  .title {
    font-weight: bold;
    font-size: 20px;
    color: coral;
  }
  .left_contain > .tit_detail{
    display: flex;
    margin-bottom: 20px;
  }
  .right_contain > .tit_detail {
    display: flex;
  }
  .sub_title {
    font-weight: bold;
    margin-top: 10px;
    color: coral;
    width: 100%;
  }
  .sub_tit_detail {
    margin-top: 10px;
    width: 100%;
  }
  .group_info {
    width: 100%;
  }
  .item_choose{
    margin-right: 5px;
    margin-left: 5px;
  }
  textarea {
    width: 100%;
    
    overflow: hidden;
    text-overflow: ellipsis;
  }
</style>