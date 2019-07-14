<template>
  <div id="app">
    <div class="layout">
      <Layout>
        <Header class="header">
          <Menu class="menu" mode="horizontal" theme="light" active-name="1">
            <div class="layout-logo">
              智慧小镇
            </div>
            <div class="layout-nav">
              <MenuItem name="1">
                <Icon class="icon" type="md-home" ></Icon>
                <router-link class="nav-item" to="/Home">首页</router-link>
              </MenuItem>
              <div>
                <Submenu name="2" >
                  <template slot="title">
                    <Icon type="md-podium" />
                    <router-link class="nav-item" to="/about" >酒店</router-link>
                  </template>
                  <MenuItem name="2-1">精选酒店</MenuItem>
                  <MenuItem name="2-2">客栈名宿</MenuItem>
                  <MenuItem name="2-3">酒店团购</MenuItem>
                </Submenu>
              </div>
              <Submenu name="3">
                <template slot="title">
                  <Icon type="md-cash" />
                  <router-link class="nav-item" to="/about" >门票</router-link>
                </template>
                <MenuItem name="3-1">周边景点</MenuItem>
                <MenuItem name="3-2">当季精选</MenuItem>
                <MenuItem name="3-3">门票预订</MenuItem>
              </Submenu>
              <Submenu name="4">
                <template slot="title">
                  <Icon type="md-restaurant" />
                  <router-link class="nav-item" to="/about" >美食</router-link>
                </template>
                <MenuItem name="4-1">热门美食</MenuItem>
                <MenuItem name="4-2">特色小吃</MenuItem>
                <MenuItem name="4-3">美食团购</MenuItem>
              </Submenu>
              <Submenu name="5">
                <template slot="title">
                  <Icon type="md-ribbon" />
                  <router-link class="nav-item" to="/about" >主题游</router-link>
                </template>
                <MenuItem name="5-1">自由行</MenuItem>
                <MenuItem name="5-2">亲子游</MenuItem>
                <MenuItem name="5-3">蜜月游</MenuItem>
                <MenuItem name="5-3">定制游</MenuItem>
              </Submenu>
              <Submenu name="6">
                <template slot="title">
                  <Icon type="md-list" />
                  <router-link class="nav-item" to="/about" >攻略</router-link>
                </template>
                <MenuItem name="6-1">推荐</MenuItem>
                <MenuItem name="6-2">游记</MenuItem>
                <MenuItem name="6-3">问答</MenuItem>
              </Submenu>
              <Submenu name="7">
                <template slot="title">
                  <Icon type="md-list" />
                  <router-link class="nav-item" to="/about" >个人中心</router-link>
                </template>
                <MenuItem name="7-1">登录/注册</MenuItem>
                <MenuItem name="7-2">我的订单</MenuItem>
                <MenuItem name="7-3">我的收藏</MenuItem>
                <MenuItem name="7-4">我的优惠券</MenuItem>
              </Submenu>
            </div>
          </Menu>
          <div class="search">
            <Input search enter-button placeholder="Enter something..." />
          </div>
        </Header>
        <Content :style="{padding:'60px 0'}">
          <Card>
            <div style="min-height:600px;"><router-view></router-view></div>
          </Card>
        </Content>
        <Footer class="layout-footer-center">2019 &copy; 北京智慧数智库科技有限公司</Footer>
      </Layout>
    </div>

  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  /*color: #2c3e50;*/
  /*margin-top: 60px;*/
  /*height: 100%;*/
}

.layout{
  border:1px solid #d7dde4;
  background: #f5f7f9;
  position: relative;
  border-radius:4px;
  overflow: hidden;
}
  .layout-logo{
    border-radius: 3px;
    float: left;
    position: relative;
    /*top: 4px;*/
    left: 30px;
    color: #2d8cf0;
    font-size: 28px;
  }
  .layout-nav{
    width: 900px;
    margin: 0 auto;
    margin-right: 20px;
  }
  .layout-footer-center{
    text-align: center;
  }
  .header{
    background: #fff;
  }
  .search{
    width: 500px;
    float: right;
    margin-right: 30px;
    margin: 16px auto;
  }
</style>
