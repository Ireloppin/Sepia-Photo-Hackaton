 <script lang="ts">
    import {originalImage, modifiedImage} from './store'
    import "two-up-element"

    /* let proccessingImage =true
    let tries = 0
    let intervalId: any

    $:{
        if(proccessingImage){
            clearInterval(intervalId)
            intervalId = setInterval(()=>{
                tries++
            }, 500)
        }
    } */
 </script>

<!-- on:load={()=>(proccessingImage = false)}
on:error={()=>(proccessingImage = true)}  -->

<two-up>
 <img src={$originalImage} alt="Imagen subida por el usuario"/>
 <img 
  
 src={`${$modifiedImage}`} alt="Imagen editada"/>
</two-up>
<div class="text-center w-full mt-8">
<a download href={$modifiedImage} class="bg-blue-500 hover:bg-blue-700 text-xl font-bols text-white rounded-full px-4 py-2 ">Descargar imagen editada</a>
</div>