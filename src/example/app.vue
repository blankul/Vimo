<template>
  <Page>
    <Header>
      <Navbar>
        <Title>App</Title>
      </Navbar>
    </Header>
    <Content padding>

      <p>
        该组件是业务页面的父组件，业务页面挂载、页面状态、弹出层挂载安插等，都是在此组件中完成。
        组件注册初始化时，会将公共下面的方法插入到Vue.prototype中，便于业务页面对ion-app组件的操控。
      </p>

      <h3>组件方法：</h3>

      <p>$setEnabled: 设置整个页面可点击状态</p>
      <p>$disableScroll: 禁止页面滚动</p>


      <Button @click="$app.setEnabled(false,3000)">3秒内页面无法点击(可滚动)</Button>

      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur in rerum saepe sed. Architecto beatae consequuntur ea id, in ipsa maxime perspiciatis, praesentium quae quo repudiandae sit tempora unde ut.</p>

      <Button @click="$app.setDisableScroll(true,3000)">3秒内页面无法滚动(无法点击+滚动)</Button>

    </Content>

  </Page>
</template>
<style scoped lang="scss">
  .main {

  }
</style>
<script type="text/ecmascript-6">
  export default{
    data(){
      return {
        isDisabled: false,
      }
    },
    watch: {},
    computed: {},
    methods: {
      disableScroll(){
        const _this = this;
        if (!_this.isDisabled) {
          _this.$app.disableScroll(true);
          _this.isDisabled = true;
          setTimeout(function () {
            _this.$app.disableScroll(false);
            _this.isDisabled = false;
          },3000)
        }
      }
    },
    created () {
    },
    mounted () {
    },
    activated () {
    },
    components: {}
  }
</script>
