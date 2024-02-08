<script setup></script>

<template>
  <div :class="$style.container">
    <h1 :class="$style.title">Latest Customers</h1>
    <h2>This is a list of latest transactions.</h2>
    <table :class="$style.table">
      <thead>
        <tr :class="$style.tr">
          <th :class="$style.post">Transaction</th>
          <th :class="$style.post">Date & time</th>
          <th :class="$style.post">Amount</th>
          <th :class="$style.post">Status</th>
        </tr>
      </thead>
      <tbody>
        <tr :class="$style.tr">
          <td>Payment from <strong>Bonnie Green</strong></td>
          <td :class="$style.date">Apr 23 ,2021</td>
          <td><strong>$2300</strong></td>
          <td><p :class="$style.completed">Completed</p></td>
        </tr>
        <tr :class="$style.tr">
          <td>Payment refund to <strong>#00910</strong></td>
          <td :class="$style.date">Apr 23, 2021</td>
          <td><strong>-$670</strong></td>
          <td><p :class="$style.completed">Completed</p></td>
        </tr>
        <tr :class="$style.tr">
          <td>Payment failed from <strong>#087651</strong></td>
          <td :class="$style.date">Apr 18, 2021</td>
          <td><strong>$234</strong></td>
          <td><p :class="$style.canceled">Cancelled</p></td>
        </tr>
        <tr :class="$style.tr">
          <td>Payment from <strong>Bonnie Green</strong></td>
          <td :class="$style.date">Apr 15, 2021</td>
          <td><strong>$5000</strong></td>
          <td><p :class="$style.progress">In progress</p></td>
        </tr>
        <tr :class="$style.tr">
          <td>Payment from <strong>Jese Leos</strong></td>
          <td :class="$style.date">Apr 15, 2021</td>
          <td><strong>$2300</strong></td>
          <td><p :class="$style.progress">In progress</p></td>
        </tr>
        <tr :class="$style.tr">
          <td>Payment from <strong>THEMSBERG LLC</strong></td>
          <td :class="$style.date">Apr 11, 2021</td>
          <td><strong>$280</strong></td>
          <td><p :class="$style.completed">Completed</p></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style module lang="scss">
  .container {
    width: calc(100vw - 32px);
    background-color: #fff;
    border-radius: 1rem;
    margin-bottom: 1rem;
    padding: 24px;
    overflow-x: scroll;
    @media (min-width: $tablet-size-land) {
      width: 100%;
      overflow-x: hidden;
    }
  }
  .title {
    margin-bottom: 0;
  }

  .table {
    width: 100%;
    min-width: 1000px;
    @media (min-width: $tablet-size-land) {
      min-width: auto;
    }
  }

  .post {
    width: 25%;
    text-transform: uppercase;
    text-align: left;
    color: #6b7280;
    font-size: 12px;
    padding: 1rem;
    border-bottom: 1px solid #e5e7eb;
  }

  .tr {
    background-color: #f9fafb;
    font-size: 14px;
    color: #111827;
    font-weight: 500;
    border-radius: 12px;
    overflow: hidden;
    border: none;
    outline: none;

    & > td {
      padding: 1rem;
      border: none;
      outline: none;
    }

    & > .date {
      font-weight: 400;
      color: #6b7280;
    }

    &:nth-child(2n) {
      background-color: #fff;
      border-radius: 0;
    }
  }

  .completed,
  .progress,
  .canceled {
    width: max-content;
    padding: 2px 10px;
    border-radius: 10px;
    font-size: 12px;
    margin: 0;
  }

  .completed {
    background-color: #def7ec;
    color: #03543f;
  }
  .progress {
    background-color: #e1effe;
    color: #1e429f;
  }
  .canceled {
    background-color: #fbd5d5;
    color: #9b1c1c;
  }
</style>
