<script>
  export let title = "";
  export let text = "";
  export let btnText = "";
</script>

<div class="sub-bg-div py-3 px-4 rounded-lg my-4">
  <div class="font-bold">
    <p class="">{title}</p>
  </div>
  
  <div class="font-medium text-xs mb-4 mt-1">
    <p class="">{text}</p>
  </div>

  <div>
    <button class="border border-slate-900 dark:border-white rounded-full px-3 bg-slate-900 text-white dark:bg-white dark:text-gray-900 dark:font-semibold py-1 text-xs">
      {btnText}
    </button>
  </div>
</div>