<script>
    let { radius = '12px', color = 'darkgreen', width = '100px' } = $props(); //use of props component
</script>

<div
class="Box"
style:border-radius={radius}
style:background-color={color}
style:width={width}
>
{color}
</div>


