<template>
    <dialog id="molang_sheet" class="dialog">
        <div class="tool close_button" @click="$emit('close')"><i class="unicode_icon">{{'\u2A09'}}</i></div>
        <h2>MoLang表</h2>
        <div class="scrollable">
            <h3>变量</h3>
            <ul>
                <li><code>variable.emitter_lifetime</code> 发射器生命周期</li>
                <li><code>variable.emitter_age</code> 发射器的寿命</li>
                <li><code>variable.emitter_random_1</code> 0到1之间的随机数, 每个发射周期中的值恒定</li>
                <li><code>variable.emitter_random_2</code> 随机数</li>
                <li><code>variable.emitter_random_3</code> 随机数</li>
                <li><code>variable.emitter_random_4</code> 随机数</li>
                <li><code>variable.particle_lifetime</code> 粒子生命周期</li>
                <li><code>variable.particle_age</code> 粒子的寿命</li>
                <li><code>variable.particle_random_1</code> 0到1之间的随机数, 每个粒子的值恒定</li>
                <li><code>variable.particle_random_2</code> 随机数</li>
                <li><code>variable.particle_random_3</code> 随机数</li>
                <li><code>variable.particle_random_4</code> 随机数</li>
                <li><code>variable.entity_scale</code> Scale of the attached entity</li>
            </ul>
            <h3>数学选项</h3>
            <ul>
                <li><code>math.abs(value)</code> 将值取绝对值</li>
                <li><code>math.sin(value)</code> 将值取正弦值</li>
                <li><code>math.cos(value)</code> 将值取余弦值</li>
                <li><code>math.clamp(value, min, max)</code> 将值限制在最小值和最大值之间（包括上限和下限）</li>
                <li><code>math.ceil(value)</code> 将值向上取整</li>
                <li><code>math.floor(value)</code> 将值向下取整</li>
                <li><code>math.trunc(value)</code> 将值向零取整</li>
                <li><code>math.round(value)</code> 将值四舍五入</li>
                <li><code>math.mod(value, denominator)</code> Return the remainder of value / denominator</li>
                <li><code>math.pow(base, exponent)</code> Elevates `base` to the `exponent`'th power</li>
                <li><code>math.sqrt(value)</code> Square root of value</li>
                <li><code>math.exp(value)</code> Calculates e to the value'th power</li>
                <li><code>math.pi</code> Returns the float representation of the constant pi.</li>
                <li><code>math.max(A, B)</code> Return highest value of A or B</li>
                <li><code>math.min(A, B)</code> Return lowest value of A or B</li>
                <li><code>math.asin(value)</code> arcsin of value</li>
                <li><code>math.acos(value)</code> arccos of value</li>
                <li><code>math.atan(value)</code> arctan of value</li>
                <li><code>math.atan2(y, x)</code> arctan of y/x. NOTE: the order of arguments!</li>
                <li><code>math.random(low, high)</code> Random value between low and high inclusive</li>
                <li><code>math.random_integer(low, high)</code> Random integer value between low and high inclusive</li>
                <li><code>math.die_roll(num, low, high)</code> returns the sum of 'num' random numbers, each with a value from low to high. Note: the generated random numbers are not integers like normal dice. For that, use `math.die_roll_integer`.</li>
                <li><code>math.die_roll_integer(num, low, high)</code> returns the sum of 'num' random integer numbers, each with a value from low to high. Note: the generated random numbers are integers like normal dice.</li>
                <li><code>math.hermite_blend(value)</code> Useful for simple smooth curve interpolation using one of the Hermite Basis functions: `3t^2 - 2t^3`. Note that while any valid float is a valid input, this function works best in the range [0,1].</li>
                <li><code>math.lerp(start, end, 0_to_1)</code> Lerp from start to end via 0_to_1</li>
                <li><code>math.lerprotate(start, end, 0_to_1)</code> Lerp the shortest direction around a circle from start degrees to end degrees via 0_to_1</li>
                <li><code>math.ln(value)</code> Natural logarithm of value</li>
            </ul>
            <a href="https://bedrock.dev/docs/stable/MoLang" target="_blank" style="margin-top: 12px; display: block;">点击查看完整的MoLang文档</a>
        </div>
    </dialog>
</template>

<script>
export default {
    name: 'molang-dialog'
}
</script>

<style scoped>
	.scrollable {
		overflow-y: scroll;
	}
	#molang_sheet code {
		padding: 2px 8px;
		color: var(--teal);
		font-size: 0.9em;
		background-color: var(--color-dark);
		user-select: text;
    }
    li {
        text-indent: -20px;
	    padding-left: 20px;
    }
</style>