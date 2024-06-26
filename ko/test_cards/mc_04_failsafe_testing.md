# 시험 MC_04 - 안전 장치 시험

❏ 원격 조종 유실 동작이 회귀 지점 착륙인지 확인

❏ 데이터 링크 유실 동작이 회귀 지점 착륙이며 10초의 제한 시간을 두는지 확인

❏ 배터리 안전 장치 검증

&nbsp;&nbsp;&nbsp;&nbsp;❏ 안전 조치 동작은 회귀 지점 착륙 동작

&nbsp;&nbsp;&nbsp;&nbsp;❏ 배터리 경고 잔여량이 25% 인가

&nbsp;&nbsp;&nbsp;&nbsp;❏ 배터리 안전 장치 가동 잔여량이 20% 인가

&nbsp;&nbsp;&nbsp;&nbsp;❏ 배터리 응급 상태 잔여량이 15% 인가

❏ 고도 제어 모드에서 이륙

❏ 기준 위치에서 최소한 20미터 이상 이동

❏ 원격 조종기 연결 유실

&nbsp;&nbsp;&nbsp;&nbsp;❏ 원격 조종 장치를 끄고 기체가 시작점으로 돌아오는지 확인, 하강 대기 후 원격 조종 장치를 켜서 제어권을 넘겨받음

## 데이터 연결 유실

❏ 텔레메트리 연결을 끊으면, 기체는 10초 후 시작 점으로 돌아와야 하며, 하강 대기 후 텔레메트리 무선 통신 장치를 다시 연결

## 고도 제어 모드 전환

❏ 좌우, 상하, 방위 회전각 응답이 안정 모드처럼 고정 값으로 응답하는지 확인

❏ 추진부에서 고도를 제어해야 하며, 스틱을 가운데로 두었을 때 고도를 유지해야 함

## 위치 제어 모드로 전환

❏ 스틱을 가운데로 두었을 때 위치를 유지해야 함

❏ 좌우, 상하, 방위 회전각을 움직여서 기체가 입력에 따라 움직이는지 확인

❏ 스틱을 가운데로 두어 기체 위치를 유지하는지 확인

## 배터리 안전 장치 가동 대기

❏ QGC에서 경고 메시지를 받는지 확인

❏ 기체가 지면으로 착륙하는지 확인

❏ 기체 착륙 확인
