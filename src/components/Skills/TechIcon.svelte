<script>
  const {imageSrc, hoverImageSrc = imageSrc, label} = $props()

  let hover = $state(false)
</script>

<div class="flex w-full flex-col items-center">
  <img
    src={hoverImageSrc}
    width="48"
    height="48"
    alt={label}
    onmouseleave={() => hover = false}
    class={`hover:scale-120 ${hover ? 'visible' : 'hidden'}`}
  />
  <img
    src={imageSrc}
    width="48"
    height="48"
    alt={label}
    onmouseenter={() => hover = true}
    class={!hover ? 'visible' : 'hidden'}
    />
  <span class="text-sm mt-4 text-center">{label}</span>
</div>

