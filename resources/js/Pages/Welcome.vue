<script setup>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'
import ApplicationLogo from '@/Components/ApplicationLogo.vue';

const navigation = [
    { name: 'შესვლა', href: '/login' },
    { name: 'რეგისტრაცია', href: '/register' },
]
</script>

<template>
    <div class="relative overflow-hidden bg-white h-screen">
        <div class="hidden sm:absolute sm:inset-y-0 sm:block sm:h-full sm:w-full" aria-hidden="true">
            <div class="relative mx-auto h-full max-w-7xl">
                <svg class="absolute right-full translate-y-1/4 translate-x-1/4 transform lg:translate-x-1/2" width="404" height="784" fill="none" viewBox="0 0 404 784">
                    <defs>
                        <pattern id="f210dbf6-a58d-4871-961e-36d5016a0f49" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                            <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
                        </pattern>
                    </defs>
                    <rect width="404" height="784" fill="url(#f210dbf6-a58d-4871-961e-36d5016a0f49)" />
                </svg>
                <svg class="absolute left-full -translate-y-3/4 -translate-x-1/4 transform md:-translate-y-1/2 lg:-translate-x-1/2" width="404" height="784" fill="none" viewBox="0 0 404 784">
                    <defs>
                        <pattern id="5d0dd344-b041-4d26-bec4-8d33ea57ec9b" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                            <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
                        </pattern>
                    </defs>
                    <rect width="404" height="784" fill="url(#5d0dd344-b041-4d26-bec4-8d33ea57ec9b)" />
                </svg>
            </div>
        </div>

        <div class="relative pt-6 pb-16 sm:pb-24">
            <Popover>
                <div class="mx-auto max-w-7xl px-4 sm:px-6">
                    <nav class="relative flex items-center justify-between sm:h-10 md:justify-center" aria-label="Global">
                        <div class="flex flex-1 items-center md:absolute md:inset-y-0 md:left-0">
                            <div class="flex w-full items-center justify-between md:w-auto">
                                <div class="flex items-center  justify-center">
                                    <img class="h-8 w-8" src="https://i.ibb.co/cTcK1PV/handshake.png" alt="handshake" >
                                    <h1 class="text-2xl ml-4 font-bold">Mentra</h1>
                                </div>
                                <div class="-mr-2 flex items-center md:hidden">
                                    <PopoverButton class="inline-flex items-center justify-center rounded-md bg-gray-50 p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
                                        <span class="sr-only">Open main menu</span>
                                        <Bars3Icon class="h-6 w-6" aria-hidden="true" />
                                    </PopoverButton>
                                </div>
                            </div>
                        </div>
                        <div class="hidden md:flex md:space-x-10">
                            <a v-for="item in navigation" :key="item.name" :href="item.href" class="font-medium text-gray-500 hover:text-gray-900">{{ item.name }}</a>
                        </div>
                        <div class="hidden md:absolute md:inset-y-0 md:right-0 md:flex md:items-center md:justify-end">

                        </div>
                    </nav>
                </div>

                <transition enter-active-class="duration-150 ease-out" enter-from-class="opacity-0 scale-95" enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in" leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
                    <PopoverPanel focus class="absolute inset-x-0 top-0 z-10 origin-top-right transform p-2 transition md:hidden">
                        <div class="overflow-hidden rounded-lg bg-white shadow-md ring-1 ring-black ring-opacity-5">
                            <div class="flex items-center justify-between px-5 pt-4">
                                <div class="flex justify-center items-center">
                                    <img class="h-12 w-12" src="https://i.ibb.co/cTcK1PV/handshake.png" alt="handshake" >
                                    <h1 class="text-2xl ml-4 font-bold">Mentra</h1>
                                </div>
                                <div class="-mr-2">
                                    <PopoverButton class="inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
                                        <span class="sr-only">Close menu</span>
                                        <XMarkIcon class="h-6 w-6" aria-hidden="true" />
                                    </PopoverButton>
                                </div>
                            </div>
                            <div class="px-2 pt-2 pb-3">
                                <a v-for="item in navigation" :key="item.name" :href="item.href" class="block rounded-md px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 hover:text-gray-900">{{ item.name }}</a>
                            </div>
                        </div>
                    </PopoverPanel>
                </transition>
            </Popover>

            <main class="mx-auto mt-16 max-w-7xl px-4 sm:mt-32 ">
                <div class="text-center">
                    <div class="text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl md:text-6xl flex flex-col items-center space-y-4">
                        <span class="block text-indigo-600 xl:inline-block pb-8">სესხი</span>
                        <span class="inline-block pb-4">ადამიანებისგან</span>
                        <img class="h-32 w-32" src="https://i.ibb.co/cTcK1PV/handshake.png" alt="handshake" >
                        <span class="inline-block pb-12">ადამიანებისთვის</span>
                    </div>
                    <p class="mx-auto mt-3 max-w-md text-base text-gray-500 sm:text-lg md:mt-5 md:max-w-3xl md:text-xl">ვაკავშირებთ ფულის გასესხების და სესხების მსურველებს</p>
                    <div class="mx-auto mt-5 max-w-md sm:flex sm:justify-center md:mt-8">
                        <div class="rounded-md shadow">
                            <a href="/register" class="flex w-full items-center justify-center rounded-md border border-transparent bg-indigo-600 px-8 py-3 text-base font-medium text-white hover:bg-indigo-700 md:py-4 md:px-10 md:text-lg">სესხება</a>
                        </div>
                        <div class="mt-3 rounded-md shadow sm:mt-0 sm:ml-3">
                            <a href="/register" class="flex w-full items-center justify-center rounded-md border border-transparent bg-white px-8 py-3 text-base font-medium text-indigo-600 hover:bg-gray-50 md:py-4 md:px-10 md:text-lg">გასესხება</a>
                        </div>
                    </div>
                </div>
            </main>
        </div>
    </div>
</template>


