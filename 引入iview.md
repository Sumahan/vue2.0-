## vue项目 引入iview
搭建完项目之后  修改src/main.js
<pre>
// The Vue build version to load with the `import` command
// (runtime-only or standalone) has been set in webpack.base.conf with an alias.
import Vue from 'vue'
import App from './App'
import router from './router'
import iView from 'iview'
import 'iview/dist/styles/iview.css'

Vue.config.productionTip = false
Vue.use(iView)

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  components: { App },
  template: '<App/>'
})
</pre>

在main.js中添加了
<pre>
import iView from 'iview'
import 'iview/dist/styles/iview.css'
Vue.use(iView)
</pre>

iview安装
<pre>
cnpm install --save iview
</pre>

使用iview，在components添加login.vue

