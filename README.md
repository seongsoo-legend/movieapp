**1**

create-react-app [파일명]으로 프로젝트를 생성할 수 있습니다.
패키지 매니저로 npm이나 yarn을 사용할 수 있는데 니콜라스선생님은 yarn을 선호합니다.
한국의 인터넷은 굉장히 빠르기 때문에 npm을 사용해서 무관합니다.
yarn start 혹은 npm strat를 터미널에 입력해서 로컬 서버를 실행합니다.

**2**

자바스크립트 안에 html코드를 JSX라고 하는데 컴포넌트를 사용할떄의 규칙입니다.
css의 경우 class를 className라고 지칭합니다.
render는 이 컴포너틑가 나에게 보여주는 것이 무엇인가 입니다.
react와 reactDOM의 차이는 react는 UI library이고
reactDOM은 리액트를 웹사이트에 출력(render)하는 것을 도와주는 모델입니다. 

import react > 컴포넌트(class) 생성 > 렌더 > 리턴 > html 내용 > 내용적고 > 브라우져 확인
컴포넌트 각가의 id를 불러오는 것은 좋은 것은 아니지만 가능합니다.

**3**

부모 컨포넌트는 props를 통해 자기 자식에게 정보를 전달 합니다.
JSX의 경우 괄호를 안치면 명령을 제대로 실행할 수 없습니다.

큰 컨포먼트가 전체 정보를 가지고 있고, 각각의 칠드런에게 정보를 전달합니다. 
UI구축에 있어서 한개의 데이터 소를 가지고 각각의 컴포넌트 별로 출력만 하면 되기 때문입니다.

**4**
이번 강의에서는 api에서 찾은 여러 정보를 배열할 수 있는 array(정렬된 항목)을 생성하는 것입니다.
map은 새로운 array를 만뜹니다.  map을 하면 새로운 array를 만드는데 다른 array를 포함한 값입니다.
 
 **5**
 
리액트는 엘리먼트가 많을 경우 key를 줘야합니다.(key는 고유해야합니다.) 또한 아큐먼트를 여러개 적을시에 ()
안에 넣어줘야 합니다. 

static propTypes를 통해 부모 컴포넌트에서 받는 정보를 체크할 수 있고 쉽게 오류를 체크할 수 있습니다. 

**6**

컴포넌트가 존재하기 시작하면 will mount -> render -> did mount 순서로 진행됩니다.
will mount 시에 api를 다운 받고 render로 뿌려준 다음에 didmount시에 마무리 해줍니다.

update시에는

componentWillReceiveProps() -> shoudComponent() -> componentWillUpdate()
componentWillReceiveProps 이미 컴포넌트를 받았다는 뜻입니다.
shoudComponent에서 props를 비교해서 이전과 새것과 다르면 업데이트를 =true 합니다.
다음 will update로 넘어가고 render후에 didmount합니다. 

componentWillMount

componentDidMount

**7**

state는 리액트 컴포넡트 안 오브젝트입니다. state가 바뀔때마다 react는 reander합니다.
setState 키워드를 이용해서 변경해줍니다.
state를 직접적으로 변경해주면 안됩니다. 꼭 setState를 이용해서 변경해줘야합니다.

**8**

setTimeout는 얼마 후에 작업을 수행시킨다는 뜻입니다. 
...(전개연산자, spread operator)는 아마 movies안의 배열의 인자를 을 전부 가져오는 것 같습니다.

**9**

state가 없는 컴포넌트는 stateless functional 컴포넌트 입니다.
그 안에는 render도 없고 라이플사이클도 없습니다. 오직 return만 있을 뿐입니다. 
변경이 없을 컴포넌트에 한해서 사용합니다.
타입 확인을 할때에는 전과 동일합니다..
 functional 컴포넌트에서는 this props를 삭제해줘야 합니다. 왜냐하면 클래스가 아니고
 이미 props를 쓰고 있기 떄문입니다.
 
 **10**
 
 JSON = JavaScript Object Notation
 Ajax는 url을 자바스크립트로 asynchronous(비동기화)방법으로 불러옵니다.
 
 **11**
 
 promise는 자바스크립트의 새로운 비동기 컨셉입니다.
 첫번째 작업이 끝날때까지 기다려야합니다. 자바사크립트는 하나에 한개밖에 처리 하지 못합니다.
 이 때 promise를 사용하면 첫번째 라인이 다 끝나기 전에 작업을 합니다.
 이것은 아마 브라우져가 하고 있는 것으로 알고 있습니다.
 즉 자바스크립트가 일할때 브라우져가 promise를 사용해서 일을 하고 있다가
 자바스크립트가 일을 다 끝내서 브라우져가 promise를 주는 걸로 알고 있습니다.
 저도 자세히 몰라서 자바스크립트 비동기라고 검색해 보시면 더 많은 정보가 나올 것입니다.
 
 에러가 있을시에 catch를 써서 오류를 표시해 줄 수 있습니다.
 then function은 1개의 attribute만 줍니다. 그리고 그것은 오브젝트(fetch의 결과물)입니다.
 
 
 **12**
 
 async는 이전 라인의 작업이 끝날떄까지 기다리지 않고 순서와 상관없이 진행됩니다.
 await는 call api 기능이 끝나는 것을 기다립니다.(성공 여부와 상관없이)
 참고로 화살표 표시(=>, arrow function)는 return이 내장되어 있기 떄문에 return을 따로 작성할 필요가 없습니다.
 id를 사용하는 이유는 컴포넌트의 key는 인덱스를 사용하면 느리기 때문입니다. 
 
 ** 13 **
 function 컴포넌트로 sapn을 리턴합니다. 직접 span을 쓸 수도 있지만
 컴포넌트 단위로 쪼개서 작게 만드는 것이 더 세련 된 것이기 때문입니다.
 