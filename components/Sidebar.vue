<template>
    <div  style="min-height: 700px" class="absolute lg:relative w-64 h-screen shadow bg-gray-100 hidden lg:block">
                    <div class="h-16 w-full flex items-center px-8">
                      <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/header-1-svg1.svg" alt="logo">
                      <br/>
                      <h2 class="font-normal text-2xl leading-6 text-gray-800">Restaja</h2>
                    </div>
                    <ul class="py-6">
                        <li class="pl-6 cursor-pointer text-white text-sm leading-3 tracking-normal pb-4 pt-5 text-indigo-700 focus:text-indigo-700 focus:outline-none">
                            <div class="flex items-center">
                                <div>
                                    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-grid" width="20" height="20" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" />
                                        <rect x="4" y="4" width="6" height="6" rx="1" />
                                        <rect x="14" y="4" width="6" height="6" rx="1" />
                                        <rect x="4" y="14" width="6" height="6" rx="1" />
                                        <rect x="14" y="14" width="6" height="6" rx="1" />
                                    </svg>
                                </div>
                                <NuxtLink to="/user" class="ml-2">Dashboard</NuxtLink>
                            </div>
                        </li>
                        <li class="pl-6 cursor-pointer text-gray-600 text-sm leading-3 tracking-normal mt-4 mb-4 py-2 hover:text-indigo-700 focus:text-indigo-700 focus:outline-none">
                            <div class="flex items-center">
                                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-puzzle" width="20" height="20" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                    <path stroke="none" d="M0 0h24v24H0z" />
                                    <path d="M4 7h3a1 1 0 0 0 1 -1v-1a2 2 0 0 1 4 0v1a1 1 0 0 0 1 1h3a1 1 0 0 1 1 1v3a1 1 0 0 0 1 1h1a2 2 0 0 1 0 4h-1a1 1 0 0 0 -1 1v3a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-1a2 2 0 0 0 -4 0v1a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1h1a2 2 0 0 0 0 -4h-1a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1" />
                                </svg>
                                <NuxtLink to="/user/nutrition" class="ml-2">Nutrition</NuxtLink>
                            </div>
                        </li>
                        <li class="pl-6 cursor-pointer text-gray-600 text-sm leading-3 tracking-normal mb-4 py-2 hover:text-indigo-700 focus:text-indigo-700 focus:outline-none">
                            <div class="flex items-center">
                                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-compass" width="20" height="20" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                    <path stroke="none" d="M0 0h24v24H0z" />
                                    <polyline points="8 16 10 10 16 8 14 14 8 16" />
                                    <circle cx="12" cy="12" r="9" />
                                </svg>
                                <NuxtLink to="/user/trainers"  class="ml-2">Trainers</NuxtLink>
                            </div>
                        </li>
                        
                    </ul>
                </div>
                <!--Mobile responsive sidebar-->
                <div class="absolute w-full h-full z-40 transform -translate-x-full lg:hidden" id="mobile-nav">
                    <div class="bg-gray-800 opacity-50 absolute h-full w-full lg:hidden" onclick="sidebarHandler(false)"></div>
                    <div class="absolute z-40 sm:relative w-64 md:w-96 shadow pb-4 bg-gray-100 lg:hidden transition duration-150 ease-in-out h-full">
                        <div class="flex flex-col justify-between h-full w-full">
                            <div>
                                <div class="flex items-center justify-between px-8">
                                    <div class="h-16 w-full flex items-center">
                                        <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/light_with_header_and_icons-svg1.svg" alt="logo">
                                    </div>
                                    <button aria-label="close sidebar" id="closeSideBar" class="flex items-center justify-center h-10 w-10 focus:outline-none focus:ring-2 focus:ring-gray-800 rounded" onclick="sidebarHandler(false)">
                                        <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/light_with_header_and_icons-svg2.svg" alt="cross">
                                    </button>
                                </div>
                                <ul class="py-6">
                                    <li class="pl-6 cursor-pointer text-white text-sm leading-3 tracking-normal pb-4 pt-5 text-indigo-700 focus:text-indigo-700 focus:outline-none">
                                        <div class="flex items-center">
                                            <div class="w-6 h-6 md:w-8 md:h-8">
                                                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-grid" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                    <path stroke="none" d="M0 0h24v24H0z" />
                                                    <rect x="4" y="4" width="6" height="6" rx="1" />
                                                    <rect x="14" y="4" width="6" height="6" rx="1" />
                                                    <rect x="4" y="14" width="6" height="6" rx="1" />
                                                    <rect x="14" y="14" width="6" height="6" rx="1" />
                                                </svg>
                                            </div>
                                            <a href="javascript:void(0)" class="ml-2 xl:text-base md:text-2xl text-base">Dashboard</a>
                                        </div>
                                    </li>
                                    <li class="pl-6 cursor-pointer text-gray-600 text-sm leading-3 tracking-normal mt-4 mb-4 py-2 hover:text-indigo-700 focus:text-indigo-700 focus:outline-none">
                                        <div class="flex items-center">
                                            <div class="w-6 h-6 md:w-8 md:h-8">
                                                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-puzzle" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                    <path stroke="none" d="M0 0h24v24H0z" />
                                                    <path d="M4 7h3a1 1 0 0 0 1 -1v-1a2 2 0 0 1 4 0v1a1 1 0 0 0 1 1h3a1 1 0 0 1 1 1v3a1 1 0 0 0 1 1h1a2 2 0 0 1 0 4h-1a1 1 0 0 0 -1 1v3a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-1a2 2 0 0 0 -4 0v1a1 1 0 0 1 -1 1h-3a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1h1a2 2 0 0 0 0 -4h-1a1 1 0 0 1 -1 -1v-3a1 1 0 0 1 1 -1" />
                                                </svg>
                                            </div>
                                            <a href="javascript:void(0)" class="ml-2 xl:text-base md:text-2xl text-base">Products</a>
                                        </div>
                                    </li>
                                    <li class="pl-6 cursor-pointer text-gray-600 text-sm leading-3 tracking-normal mb-4 py-2 hover:text-indigo-700 focus:text-indigo-700 focus:outline-none">
                                        <div class="flex items-center">
                                            <div class="w-6 h-6 md:w-8 md:h-8">
                                                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-compass" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                    <path stroke="none" d="M0 0h24v24H0z" />
                                                    <polyline points="8 16 10 10 16 8 14 14 8 16" />
                                                    <circle cx="12" cy="12" r="9" />
                                                </svg>
                                            </div>
                                            <a href="javascript:void(0)" class="ml-2 xl:text-base md:text-2xl text-base">Performance</a>
                                        </div>
                                    </li>
                                    <li class="pl-6 cursor-pointer text-gray-600 text-sm leading-3 tracking-normal py-2 hover:text-indigo-700 focus:text-indigo-700 focus:outline-none">
                                        <div class="flex items-center">
                                            <div class="w-6 h-6 md:w-8 md:h-8">
                                                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-code" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                    <path stroke="none" d="M0 0h24v24H0z" />
                                                    <polyline points="7 8 3 12 7 16" />
                                                    <polyline points="17 8 21 12 17 16" />
                                                    <line x1="14" y1="4" x2="10" y2="20" />
                                                </svg>
                                            </div>
                                            <a href="javascript:void(0)" class="ml-2 xl:text-base md:text-2xl text-base">Deliverables</a>
                                        </div>
                                    </li>
                                </ul>
                            </div>
                            <div class="w-full">
                                <div class="flex justify-center mb-4 w-full px-6">
                                    <div class="relative w-full">
                                        <div class="text-gray-600 absolute ml-4 inset-0 m-auto w-4 h-4">
                                           <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/light_with_header_and_icons-svg3.svg" alt="Search">
                                        </div>
                                        <input class="bg-gray-200 focus:outline-none rounded w-full text-sm text-gray-600 placeholder-gray-600 pl-10 py-2" type="text" placeholder="Search" />
                                    </div>
                                </div>
                                <div class="border-t border-gray-300">
                                    <div class="w-full flex items-center justify-between px-6 pt-1">
                                        <div class="flex items-center">
                                            <img alt="profile-pic" role="img" src="https://tuk-cdn.s3.amazonaws.com/assets/components/boxed_layout/bl_1.png" class="w-8 h-8 rounded-md" />
                                            <p class="md:text-xl text-gray-800 text-base leading-4 ml-2">Jane Doe</p>
                                        </div>
                                        <ul class="flex">
                                            <li class="cursor-pointer text-white pt-5 pb-3">
                                                <a aria-label="open chats" href="javascript:void(0)">
                                                   <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/light_with_header_and_icons-svg4.svg" alt="chats">
                                                </a>
                                            </li>
                                            <li aria-label="open notifications" class="cursor-pointer text-white pt-5 pb-3 pl-3">
                                                <a aria-label="open notifications"  href="javascript:void(0)">
                                                   <img src="https://tuk-cdn.s3.amazonaws.com/can-uploader/light_with_header_and_icons-svg5.svg" alt="notifications">
                                                </a>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
</template>