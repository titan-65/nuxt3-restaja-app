<script setup>
//FIXME: Layout of custom-user is not working after login and logout
//TODO: Add a watcher or watchEffect to check when the route changes

const { supabase } = useSupabase()
const router = useRouter()

const signOut = async () => {
  const {error} = supabase.auth.signOut()
    if (error) {
        console.log(error)
    }
  router.push('/')
}
</script>
<template>
    <div>
        <div class="2xl:container 2xl:mx-auto">
            <div class="bg-gray-200 rounded shadow-lg py-5 px-7">
                <nav class="flex justify-between">
                    <div class="flex items-center space-x-3 lg:pr-16 pr-6">
                        <img class="cursor-pointer" src="https://tuk-cdn.s3.amazonaws.com/can-uploader/header-1-svg1.svg" alt="circle" />                       
<!--                        <h2 class="font-normal text-2xl leading-6 text-gray-800">OvonRueden</h2>-->
                                            <div class=" h-full w-2 border-l border-gray-400"></div>

                    </div> 
                    <ul class="hidden md:flex flex-auto space-x-2">
                        <li @click="signOut" class="focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 text-white bg-indigo-600 cursor-pointer px-3 py-2.5 font-normal text-xs leading-3 shadow-md rounded">Logout</li>
                       
                    </ul>
                    <div class=" flex space-x-5 justify-center items-center pl-2">
                        <div class="relative cursor-pointer focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 ">
                           <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/header-1-svg2.svg" alt="chat" />  
                            <div class="animate-ping w-1.5 h-1.5 bg-indigo-700 rounded-full absolute -top-1 -right-1 m-auto duration-200"></div>
                            <div class=" w-1.5 h-1.5 bg-indigo-700 rounded-full absolute -top-1 -right-1 m-auto shadow-lg"></div>
                        </div>
                        
                      <img class="cursor-pointer  focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 " src="https://tuk-cdn.s3.amazonaws.com/can-uploader/header-1-svg3.svg" alt="bell" />                      
                    </div>
                </nav>
    
                <div class="block md:hidden w-full mt-5 ">
                    <div onclick="selectNew()" class="cursor-pointer px-4 py-3 text-white bg-indigo-600 rounded flex justify-between items-center w-full">
                        <div class="flex space-x-2">
                            <span id="s1" class="font-semibold text-sm leading-3 hidden">Selected: </span><p id="textClicked" class="font-normal text-sm leading-3 focus:outline-none hover:bg-gray-800 duration-100 cursor-pointer ">Collections</p>
                        </div>
                        <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/header-1-svg4.svg" alt="down arrow" />                    
                    </div>
                    <div class=" relative">
                        <ul id="list" class=" hidden font-normal text-base leading-4 absolute top-2  w-full rounded shadow-md">
                            <li onclick="selectedSmall()" class="px-4 py-3 text-gray-600 bg-gray-50 border border-gray-50 focus:outline-none focus:bg-gray-100 hover:bg-gray-100 duration-100 cursor-pointer text-xs leading-3 font-normal">Arts</li>
                            <li onclick="selectedSmall()" class="px-4 py-3 text-gray-600 bg-gray-50 border border-gray-50 focus:outline-none focus:bg-gray-100 hover:bg-gray-100 duration-100 cursor-pointer text-xs leading-3 font-normal">Space</li>
                            <li onclick="selectedSmall()" class="px-4 py-3 text-gray-600 bg-gray-50 border border-gray-50 focus:outline-none focus:bg-gray-100 hover:bg-gray-100 duration-100 cursor-pointer text-xs leading-3 font-normal">Game</li>
                            <li onclick="selectedSmall()" class="px-4 py-3 text-gray-600 bg-gray-50 border border-gray-50 focus:outline-none focus:bg-gray-100 hover:bg-gray-100 duration-100 cursor-pointer text-xs leading-3 font-normal">Utility</li>
                            <li onclick="selectedSmall()" class="px-4 py-3 text-gray-600 bg-gray-50 border border-gray-50 focus:outline-none focus:bg-gray-100 hover:bg-gray-100 duration-100 cursor-pointer text-xs leading-3 font-normal">Cards</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
      </div>
    
</template>