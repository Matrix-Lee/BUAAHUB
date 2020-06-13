<template>
<div>
    <div class="tt-wrapper-section">
        <div class="container">
            <div class="tt-user-header">
                <div class="tt-col-avatar">
                    <div class="tt-icon">
                       <svg class="tt-icon">
                          <use xlink:href="#icon-ava-d"></use>
                        </svg>
                    </div>
                </div>
                <div class="tt-col-title">
                    <div class="tt-title">
                       <router-link to="/User">{{username}}</router-link>
                    </div>
                    <ul class="tt-list-badge">
                        <li><a href="#"><span class="tt-color14 tt-badge">{{rank}}</span></a></li>
                    </ul>
                </div>
                <div class="tt-col-btn" id="js-settings-btn">
                    <div class="tt-list-btn">
                        <a href="#" class="tt-btn-icon">
                            <svg class="tt-icon">
                              <use xlink:href="#icon-settings_fill"></use>
                            </svg>
                        </a>
                        <a href="#" class="btn btn-primary">私信</a>
                        <a href="#" class="btn btn-secondary">关注</a>
                    </div>
                </div>
            </div>
        </div>
    </div>

 <div class="container">
    <div class="tt-tab-wrapper">
         <div class="tt-tab-wrapper">
            <div class="tt-wrapper-inner">
                <ul class="nav nav-tabs pt-tabs-default" role="tablist">
                    <li class="nav-item">
                        <a class="nav-link " data-toggle="tab" href="#tt-tab-01" role="tab">
                            <span><router-link to="/User" class="link">动态 </router-link></span>
                        </a>
                    </li>
                    <li class="nav-item show">
                        <a class="nav-link active" data-toggle="tab" href="#tt-tab-02" role="tab">
                            <span>
                             <router-link to="/UserTiezi" class="link">帖子 </router-link>
                            </span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" data-toggle="tab" href="#tt-tab-03" role="tab">
                            <span>
                            <router-link to="/UserReply" class="link">回复 </router-link>
                            </span></a>
                    </li>
                   
                    <li class="nav-item tt-hide-md">
                        <a class="nav-link" data-toggle="tab" href="#tt-tab-05" role="tab"><span><router-link to="/UserCollect" class="link">收藏 </router-link></span></a>
                    </li>
                    
                </ul>
            </div>
         </div>
    
         <div class="tab-content">
                <div class="tab-pane tt-indent-none  show active" id="tt-tab-01" role="tabpanel">
                   <div class="tt-topic-list">

                    <div class="tt-list-header">
                            <div class="tt-col-topic">帖子</div>
                            <div class="tt-col-value-large hide-mobile">分类</div>
                            <div class="tt-col-value-large hide-mobile">状态</div>
                            <div class="tt-col-value-large hide-mobile">日期</div>
                    </div>




        
                   </div>
                </div>
         </div>


    </div>
 </div>

</div>
</template>





<script>
import Vue from "vue";

export default {
  name: 'UserTiezi',
  computed: {
    username: function() {
      if (this.$store.state.isLogin) {
        return this.$store.state.user.username;
      } else return "未登录";
    },
    rank: function() {
      if (this.$store.state.isLogin) {
        return this.$store.state.user.rank;
      } else return "0";
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import "../assets/user.css"

</style>