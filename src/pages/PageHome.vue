<template>
  <q-page>
    <div class= "q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col" >
        <q-input bottom-slots class= "new-post" v-model="newPost" placeholder="What's up..!" counter maxlength="300" autogrow>
        <template v-slot:before>
          <q-avatar size="xl">
            <img src="https://cdn.quasar.dev/img/avatar4.jpg">
          </q-avatar>
        </template>

       
       

       <!-- <template v-slot:after>-->
          
       <!-- </template>-->
      </q-input> 

      </div>
      <div class="col col-shrink" >
        <q-btn class="q-mb-lg" unelevated rounded color="primary" label="Post" no-caps :disable="!newPost" />

      </div>
      
    </div>
    
<q-separator size="10px"/>
<q-list>
      <q-item-label header>TimeLine</q-item-label>

      <q-item class="q-py-md">
        <q-item-section avatar>
          <q-avatar size="xl">
            <img src="https://cdn.quasar.dev/img/avatar4.jpg">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitble1">
            <strong>Sherlock </strong> 
            <span class="text-grey-7">@holmes</span>
            </q-item-label>
          <q-item-label>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
            Molestiae tenetur odio, delectus ex nostrum voluptas dignissimos 
            qui aspernatur nobis nisi eaque perferendis, quod nemo quis aliquam maxime quibusdam, nulla deserunt.
          </q-item-label>
        </q-item-section>

        <q-item-section side top>
          1 min ago
        </q-item-section>
      </q-item>

      <q-separator inset="item" />

      <q-item class="q-py-md">
        <q-item-section avatar>
          <q-avatar size="xl">
            <img src="https://cdn.quasar.dev/img/avatar4.jpg">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitble1">
            <strong>Sherlock </strong> 
            <span class="text-grey-7">@holmes</span>
            </q-item-label>
          <q-item-label>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
            Molestiae tenetur odio, delectus ex nostrum voluptas dignissimos 
            qui aspernatur nobis nisi eaque perferendis, quod nemo quis aliquam maxime quibusdam, nulla deserunt.
          </q-item-label>
        </q-item-section>

        <q-item-section side top>
          1 min ago
        </q-item-section>
      </q-item>
      <q-separator inset="item" />


    </q-list>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageHome',
  data(){
    return{
      newPost : ''

    }
  }
})
</script>

<style lang="sass">
.new-post
  textarea
    font-size: 17px
    line-height: 1.2 !important
</style>