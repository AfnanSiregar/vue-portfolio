<template>
<div class="flex fixed justify-end items-center space-x-2 mx-auto z-10 right-0 top-[85px] py-2 px-2">
    <div class="hover:animate-pulse">
        <label for="checkbox" class="switch">
            <input @click="mode()" type="checkbox" id="checkbox" hidden />
            <div class="slider round"></div>
        </label>
    </div>
</div>
</template>

<script>
export default {
    methods:{
        mode(){
            const checkbox = document.querySelector("#checkbox");
            const html = document.querySelector("html");

            const toggleDarkMode = function () {
                checkbox.checked
                    ? html.classList.add("dark")
                    : html.classList.remove("dark");
            }

            toggleDarkMode();
            checkbox.addEventListener("click", toggleDarkMode);
        }
    }
}
</script>

<style>
.switch {
    display: inline-block;
    height: 24px;
    position: relative;
    width: 50px;
}

.switch input {
    display: none;
}

.slider {
    background-color: #ccc;
    bottom: 0;
    cursor: pointer;
    left: 0;
    position: absolute;
    right: 0;
    top: 0;
    transition: .4s;
}

.slider:before {
    background-color: #fff;
    bottom: 4px;
    content: "";
    height: 16px;
    left: 4px;
    position: absolute;
    transition: .4s;
    width: 16px;
}

input:checked+.slider {
    background-color: #f59e0b;
}

input:checked+.slider:before {
    transform: translateX(26px);
}

.slider.round {
    border-radius: 34px;
}

.slider.round:before {
    border-radius: 50%;
}
</style>