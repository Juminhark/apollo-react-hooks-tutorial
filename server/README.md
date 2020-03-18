https://ultimatecourses.com/blog/graphql-subscriptions-with-apollo-server-and-client#server-setup

https://github.com/zackify/graphql-course/tree/master/server/src

서버 개발에 대해 이해도가 있다면 graphql-yoga로 빠르게 서버를 개발할수있다.

GraphQL에는 query와 mutation 그리고 subscription 이렇게 총 3가지 operation type이 있다

 query는 데이터 조회를 위해서 필수적으로 사용되고, mutation은 데이터 변경을 위해서 많이 사용되고 있다

 query와 mutation 대비 다소 생소한 subscription은 주로 실시간(real-time) 애플리케이션을 구현하기 위해서 사용

 subscription도 기본적으로 query처럼 데이터를 조회를 위해서 사용되지만 작동 방식에서 큰 차이가 있다

 query와 mutation은 전통적인 서버/클라이언트(server/client) 모델을 따르는 반면에, subscription은 발행/구독(pub/sub) 모델을 따른다

 server/client 모델에서는 클라이언트에서 최신의 데이터를 받아오려면, 더 자주 서버를 호출하는 방법 밖에 없는데,
접속자가 많은 서버에서 동시 다발적으로 변경이 발생하는 경우 클라이언트에서 아무리 자주 호출하더라도 완벽한 실시간을 달성하기는 어렵다.

pub/sub 모델을 따르는 GraphQL의 subscription은 서버에서 발생하는 이벤트를 클라이언트에서 좀 더 효과적으로 인지할 수 있도록 해준다.
query와 mutation이 HTTP 프로토콜을 사용하는 반면에, subscription은 Web Socket 프로토콜을 사용한다.
Web Socket을 사용하면 클라이언트는 서버와 연결 채널을 유지한체로, 서버에서 발생하는 이벤트를 실시간으로 수신받을 수 있다.