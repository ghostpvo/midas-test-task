<template>
  <div class="b-wrap buttons-demo">
    <Button
      :title="'BTN BIG'"
      class="bg-blue-light"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-blue"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-blue-dark"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-black-blue"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-blue-light"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-blue"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-white-light"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-white"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-white-dark"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-black-red"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-red-light"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-red"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-blue-light white-borders"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-blue white-borders"
    />
    <Button
      :title="'BTN BIG'"
      class="bg-blue-dark white-borders"
    />
  </div>
</template>

<script>
import Button from '../../Elements/Button/Button'
export default {
  name: 'Buttons',
  components: { Button }
}
</script>

<style lang="scss" scoped>
  .buttons-demo {
    width: 1100px;
    padding-bottom: 100px;

    .button-main {
      display: inline-block;
      margin: 50px 50px 0 0;
    }
  }
</style>
