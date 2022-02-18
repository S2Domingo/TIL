# HTTP vs WebSocket
HTTP와 WebSocket은 클라이언트와 서버 커뮤니케이션에 사용되는 프로토콜이다. Application layer에 위치, Transport layer에 의존해 통신한다. 

## HTTP

Stateless
- HTTP 또는 HTTPS 요청이 매번 서버에 대해 새 연결을 설정 -> 응답을 받음 -> 연결 종료
- HTTP 포트는 80, HTTPS 포트는 443

- Client의 요청에 의해서만 서버가 응답해서 정보를 전송하고, 곧바로 연결을 끊는 방식이다.
- Client가 요청을 보내고 server가 응답하는 단방향통신(연결상태유지x)
- 서버에서는 클라이언트에 메세지를 보낼 수 없음. 
- 서버는 클라이언트의 데이터를 저장하지 않고, 클라이언트가 보내는 세션과 쿠키를 사용하여 상태를 유지한다. 

ex) 실시간 통신이 필요하지 않은 상황. Simple RESTful 애플리케이션

## WebSocket

Stateful
- HTTP 연결보다 빠르다.
- ws, wss 프로토콜
- 포트는 ws는 80, wss는 443으로 HTTP와 같다

- Client와 Sever가 실시간으로 양방향 통신을 하는 방식.  (전이중 통신)
- 서버 역시 클라이언트한테 요청을 보낼 수 있다.
- 클라이언트와 서버는 TCP 포트를 통해 지속적으로 통신한다. 


ex) Real-time 웹 애플리케이션(trading, monitoring, notification), Gaming 애플리케이션, Chat 애플리케이션

[Source](https://www.geeksforgeeks.org/what-is-web-socket-and-how-it-is-different-from-the-http/#:~:text=HTTP%20Connection,the%20client%20or%20the%20server.)