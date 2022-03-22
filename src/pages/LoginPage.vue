<template>
  <q-page class="flex flex-center" padding>
    <!-- content -->
    <div class="full-width" style="max-width:350px">
      <h5 class="q-my-md text-center">
        Login
        </h5>
      <q-card class="bg-green">
        <q-card-section>
        <q-form>
            <q-input label="Email" type="email"
          filled
          placeholder="dawascope@gmail.com" />
          <q-input
          label="Password"
          filled
          type="password"
          class="q-mt-md"
          />
          <q-checkbox
          label="Remember me"
          :model-value="true">

          </q-checkbox>
        </q-form>
        </q-card-section>
         <q-btn type="submit"
          color="grey"
          label="Login"

          class="full-width"
          />
      </q-card>
    </div>
  </q-page>
</template>

<script>
export default {
  // name: 'PageName',
}
</script>
