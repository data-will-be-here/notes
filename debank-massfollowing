function nextPage() {
  const queryString = window.location.search;
  const urlParams = new URLSearchParams(queryString);
  const start = urlParams.get('start') ? urlParams.get('start') : 0
  let newPage = document.querySelector('.db-talbe-pagination').querySelectorAll('li')[start / 100 + 2]
  if (newPage) newPage.click();
}

function action() {
  let goods = 0
  document.querySelectorAll('.db-table-row').forEach((e, i1, arr1) => {
    let i = 0
    e.querySelectorAll('.db-table-cell').forEach((el, i2, arr2) => {
      i++;
      if (i == 6) {
        let button = el.querySelector('.FollowButton_followBtnIcon__cZE9v')
        goods += 1
        let time = 1000 + goods * 100;
        setTimeout(function () {
          button.click()
          if (i1 === arr1.length - 1 && i2 === arr2.length - 1) {
            nextPage(),
                setTimeout(function() { action() }, time + 3000)
          }
        }, time)
      }


    })
  })
}

action()
