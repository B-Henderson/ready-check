<template>
  <form
    action="https://docs.google.com/forms/d/e/1FAIpQLSdZDxcliECJVNznS7wudM8C27_udu8J_22YK4FtX0J9mZ-C6Q/formResponse"
    method="POST"
  >
    <div class="apply-container">
      <div class="info-sec">
        <div class="data-key">Character Name:</div>
        <input class="form-input" type="text" v-model="character" name="entry.673427285">
      </div>
      <div class="info-sec">
        <div class="data-key">Class:</div>
        <input class="form-input" type="text" v-model="classname" name="entry.45637087">
      </div>
      <div class="info-sec">
        <div class="data-key">Spec:</div>
        <input class="form-input" type="text" v-model="spec" name="entry.500635604">
      </div>
      <div class="info-sec">
        <div class="data-key">Please provide your Battletag</div>
        <input class="form-input" type="text" v-model="btag" name="entry.1847137457">
      </div>
      <!-- <div class="info-sec checkbox-container">
        <div class="data-key">What are your main interests in wow:</div>
        <div class="checkgroup">
          <label class="checkbox">
            <div>Raiding</div>
            <input value="raiding" name="raiding" type="checkbox" v-model="interests">
            <div class="checkmark">
              <span class="checkmark-span"></span>
            </div>
          </label>
          <label class="checkbox">
            <div>PvP</div>
            <input value="pvp" name="pvp" type="checkbox" v-model="interests">
            <div class="checkmark">
              <span class="checkmark-span"></span>
            </div>
          </label>
          <label class="checkbox">
            <div>Social</div>
            <input value="social" name="social" type="checkbox" v-model="interests">
            <div class="checkmark">
              <span class="checkmark-span"></span>
            </div>
          </label>
          <label class="checkbox">
            <div>Leveling</div>
            <input value="leveling" name="leveling" type="checkbox" v-model="interests">
            <div class="checkmark">
              <span class="checkmark-span"></span>
            </div>
          </label>
        </div>
      </div>             -->
      <div class="info-sec">
        <div class="data-key">Do you have any raiding experience? :</div>
        <textarea class="form-area" placeholder="max 255 characters" rows="5" maxlength="255" cols="30" maxtype="textarea" v-model="experience" name="entry.749355333"/>
      </div>
    <div class="info-sec">
      <button type="submit">Submit</button>
    </div>
    </div>
  </form>
</template>
<script>
export default {
  data: function() {
    return { character: "", classname: "", spec: "", interests: [], experience: "", btag: "" };
  },
  methods: {
    dataform() {
    }
  }
};
</script>
<style lang="scss">
.info-sec{
  button{
    background-color: rgba(0,0,0,0);
    color: #eee;
    padding: 10px;
    border: 1px solid rgba(200, 163, 15, 1);
    &:hover{
      background-color: #333;
      color: rgba(200, 163, 15, 1);
      cursor:pointer;
    }
  }
}
.checkgroup {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;

  .checkbox {
    flex: 0 50%;
    padding: 2px;
    display: flex;
    cursor: pointer;
    user-select: none;
    justify-content: space-between;
    &:hover {
      text-decoration: underline;
    }
    .checkmark {
      display: block;
      height: 25px;
      position: relative;
      width: 25px;
      background-color: #333;
      box-shadow: 0px 0px 2px 0px rgba(200, 163, 15, 1);
      margin-left: 1rem;
      span {
        &::after {
          content: "";
          position: absolute;
          display: none;
          left: 9px;
          top: 5px;
          width: 5px;
          height: 10px;
          border: solid rgba(200, 163, 15, 1);
          border-width: 0 3px 3px 0;
          -webkit-transform: rotate(45deg);
          -ms-transform: rotate(45deg);
          transform: rotate(45deg);
        }
      }
    }

    input[type="checkbox"] {
      &:checked + div {
        span {
          &::after {
            display: block;
          }
        }
      }
      position: absolute;
      opacity: 0;
      cursor: pointer;
      height: 0;
      width: 0;
    }
  }
}
.form-input {
  background-color: rgba(0, 0, 0, 0);
  border: none;
  border-bottom: 1px solid rgba(200, 163, 15, 1);
  color: #eee;
  text-align: center;
}
.form-area {
  border: 1px solid rgba(200, 163, 15, 1);
  background-color: rgba(0, 0, 0, 0);
  color: #eee;
}
</style>

