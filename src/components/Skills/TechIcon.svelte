<script>
  const {imageSrc, hoverImageSrc = imageSrc, label} = $props()

  let hover = $state(false)
</script>

<div class="flex w-full flex-col items-center">
  <img
    src={hover ? hoverImageSrc : imageSrc}
    width="48"
    height="48"
    alt={label}
    onmouseenter={() => hover = true}
    onmouseleave={() => hover = false }
    class="hover:scale-120"
  />
  <span class="text-sm mt-4 text-center">{label}</span>
</div>

