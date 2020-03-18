https://github.com/apollographql/subscriptions-transport-ws 

https://ultimatecourses.com/blog/graphql-subscriptions-with-apollo-server-and-client
 
 GraphQL의 subscription은 Web Soket 프로토콜을 사용하기 때문에 apollo-link-http 대신에 apollo-link-ws 패키지를 설치해줘야 한다는 점입니다.
subscriptions-transport-ws 패키지는 apollo-link-ws 패키지가 필요로 하기 때문에 함께 설치가 되야합니다.