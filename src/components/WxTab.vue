
<script>
import TabNav from './tab-nav.vue'
export default {
  name:'WxTabs',
  components:{
    TabNav
  },
  render(h) {
    console.log('h :', h);
    let {currentName} = this
    const navData = {
      ref: 'nav',
      props: {
        currentName
      }
    }
    const header= (
      <div>
        <tab-nav {...navData}></tab-nav>
      </div>
    )
    const panels= (
      <div>
        {this.$slots.default}
      </div>
    )
    return (
      <div>
        {[header,panels]}
      </div>
    )
  }
}
</script>

<style>

</style>