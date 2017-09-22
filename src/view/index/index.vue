<template>
  <div class="hello"> 
    <search></search>
    <image_a></image_a>
    <myOption></myOption>
    <myNotice></myNotice>
    <myContent></myContent>
    <myFooter></myFooter>
  </div> 
</template>

<script>
import image_a from '@/components/header/image'
import search from '@/view/header/search'
import myOption from '@/components/options/option'
import myNotice from '@/components/notice/notice'
import myContent from '@/components/content/content'
import myFooter from '@/components/footer/footer'
import {api} from '@/api'

export default {
    name: 'hello',
  // created(){
  //    this.$http({
  //       url:'index.php?m=shop&c=video_interface&a=video_like',
  //       method:'get',
  //       params:{

  //       }, 
  //    }).then((res)=>{
  //     // let data = res.data; 
  //       console.log(res.data)
  //       this.obj = res.data;
  //     // data=null;
  //    })
  // },
    components:{
      search,image_a,myOption,myNotice,myContent,myFooter
    },
  // created(){ 
  //   // const val = '111111'
  //   ////////////////////////////////////
  //   // alerts(`dadssa${val}sadasdsa`) //
  //   ////////////////////////////////////
  //    // console.log(api)
  // },
  // methods:{
     
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

