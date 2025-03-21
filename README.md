# --수정 예정--

[로켓부스트]블록체인 엔지니어 부트캠프 OT
25.01.31

-전반적인 커리큘럼 강의
-내일배움카드 신청 익일 수강신청
-비트코인 백서읽어보기
-하루에 한번 블로그작성하기


터미널 연습
Last login: Fri Jan 31 11:19:11 on console
sh@Sui-MacBookPro ~ % pwd       
/Users/sh
sh@Sui-MacBookPro ~ % ls
Desktop		Downloads	Movies		Pictures
Documents	Library		Music		Public
sh@Sui-MacBookPro ~ % cd Desktop
sh@Sui-MacBookPro Desktop % pwd
/Users/sh/Desktop
sh@Sui-MacBookPro Desktop % mkdir 임한수
sh@Sui-MacBookPro Desktop % ls
임한수
sh@Sui-MacBookPro Desktop % touch test.txt
sh@Sui-MacBookPro Desktop % ls
test.txt	임한수
sh@Sui-MacBookPro Desktop % cd 임한수
sh@Sui-MacBookPro 임한수 % touch test.txt
sh@Sui-MacBookPro 임한수 % ls
test.txt
sh@Sui-MacBookPro 임한수 % vim test.txt

논릭적사고문제
1. [12,38,91,45,23,7,5]
2. A
3. 4
4. [D,C,A,B,E] 345
5. (2,5)(5,3)(3,6)(6,1)
6. 규칙:+4+2씩 숫자:42
7. 9,18,27,36,39,48
8. C
9. 4213
10. 규칙:앞의 숫자 + x*2 숫자:63


-2월3일 
블록체인은 데이터를 블록단위로 저장하고 이를 체인형태로 연결하여 분산된 네트워크에서 관리하는 기술입니다. 중앙기관없이 참여자들이 공동으로 데이터를 검증하고 저장하는 **분산 원장 기술(DLT)**의 한 형태입니다.

블록채인의 주요 특징 
탈중앙화: 중앙 기관 없이 P2P 네트워크로 운영
변조 불가능성: 데이터를 위조하거나 수정할 수 없음
보안성: 암호화 기술을 활용해 높은 신뢰성 보장
투명성: 누구나 거래내역을 확인할 수 있음
스마트 컨트렉트: 자동화된 계약 기능 제공

-블록체인 기술의 기원과 등장 이유
1. 신뢰 문제 해결
기존 금융 시스템에서는 **중앙기관(은행,정부0**이 신뢰를 보장하지만, 높은 수수료, 거래지연, 데이트 조작가능성 이런 문제를 해결하기 위해 블록체인 등장
2. 비트코인의 등장
**2008년, 사토시 나카모토**가 비트코인 백서를 발표하면서 블록체인의 개념이 구체화
중앙기관 없이도 개인간(P2P)송금가능
이중 지불(Double Spending)문제해결
높은 수수료와 거래 속도 문제 개선

타임스탬프는 데이터가 생성되거나 변경된 시간정보를 기록하는 것을 의미
주요기능
데이터 무결성보장(변조 방지)
순서 보장(이전 기록과의 관계유지)
보안성 강화(전자 문서, 금융 거래 인증)
이력관리(로그 데이터 저장)

예시(UTC형식): 2025-02-03ㅅT14:35:22Z (ISO 8601형식)

-2울4일-
해시(Hash)는 데이터를 압축하고 고정된 크기의 출력 값

데이터의 무결성을 확인/ 암호학적 보안 제공

-단방향성

해시값에서 원래 데이터를 되돌릴 수 없음

망고에서 망고주스 O

망고주스에서 망고 X

-충돌 저항성

서로 다른 입력 값이 같은 해시 값을 가질 확률이 극히 낮음

-빠른 연산 속도

블록체인에서 해시는 빠르게 계산 할 수 있어 블록체인 트렌젝션 검증과 무결성 확인에 사용 

해시의 역할 

1. 블록의 고유 식별자 역할

블록체인의 각 블록은 이전 블록의 해시 값을 포함하여 연결

하나의 블록이 변조될 경우 이후 모든 블록의 해시 값이 바뀌어 변조를 쉽게 탐지

1. 트렌젝션 무결성 검증

트렌젝션이 해시 값을 사용하여 기록

3.마클 트리 구조

블록체인에서 트렌젝션 데이터를 효율적으로 관리하기 위해 해시 트리를 사용 

트렌젝션들의 해시 값을 결합하여 최종적으로 하나의 해시 값(머클 루트)을 만듦

이를 통해 빠르게 데이터의 무결성을 검증

블록체인 대표 해시 함수

1. SHA-256

비트코인, 이더리움 등에서 사용되는 해시 함수

256비트의 고정된 길이 출력 값을 생성

1. Keccak -256 (SHA-3)

이더리움에서 사용되는 해시 함수

SHA-256과 유사하지만 구조적으로 조금 다름

1. RIPEMD-160

비트코인의 주소 생성 과정에서 사용됨

SHA-256을 거친 후, RIPEMD-160을 적용하여 짧은 해시 값을 생성

-블록 해시(block hash)

해당 블록의 고유한 식별자로 사용되는 해시값

-블록 해시 값 생성 인자(데이터)

1. 이전 블록의 해시값
2. 머클루트(merkle root): 블록 내 모든 트렌잭션의 요약 값
3. Timestamp
4. 난이도 목표(Difficulty Target): 작업 증(poW)에서 필요한 해시의 난이도
5. 논스(Nonce): 작업 증명을 완료하기 위해 반복적으로 변경되는 값

→위의 데이터를 결합하여, SHA-256 해시 함수를 두번 적용해서 블록 해시 값을 생성

작업 증명 (poW)

블록체인의 합의 알고리즘 중 하나로 새로운 블록을 추가할 때 특정한 연산 작업(채굴)을 수행해야하는 방식 

네트워크의 보안을 유지하고, 트렌잭션을 검증하며, 분산 합의를 이루기위해 사용

트렌잭션 ID(TXID)

블록체인에서 특정 트렌잭션을 식별하는 고유한 해시 값

입력, 출력, 금액 등이 데이터에 포함

머클 트리(Merkle tree)

블록체인에서 트렌잭션 데이터를 효올적으로 검증하고  저장하기위해 사용되는 트리구조의 데이터 구조

각 노드는 트렌잭션 데이터의 해시 값이며, 부모 노드는 자식 노드 두개의 해시 값을 결합하여 다시 해싱한 값으로 구성됨

-머클트리의 역할

1. 블록체인의 데이터 무결성 보장
2. 뻐른 트랜젝션 검증(SPV,간이 검증)
3. 효율적인 데이터 저장

비트코인 주소 생성

비트코인의 주소 체계에는 비대칭키 암호화를 기반으로 생성되는데, 이 비대칭키 암호화에서는 공개키와 비밀키가 사용됨

디지털 서명 

트렌잭션의 무결성을 보장, 소유권을 증명하는 암호화 기술

-디지털 서명의 동작과정

1. 해싱(Hashing)

원본 메시지를 해시 함수로 변환하여 고정된 길이의 해시 값을 생성

1. 서명(Signing)

생성된 해시값을 서명자의 개인키로 암호화하여 디지털 서명 생서

1. 검증 (Verification)

수신자는 서명자의 공개키를 사용하여 서명이 올바른지 검증

암호화 (Encryption)

데이터를 보호하기 위해 원본 정보를 특정 알고리즘을 사용하여 변환하는 과정 

암호화된 데이터는 허가된 사용자만 복호화(Decryption)하여 읽을 수 있도록 보안성을 제안

은닉(Confidentiality)

데이터를 암호화하여 비인가된 사용자가 해당 데이터를 읽지 못하도록 보호하는 개념

증명(Integrity and Authenticity)

암호화를 이용하여 데이터의 무결성과 인증을 보장하는 개념

디지털 서명이 암호화의 증명에 사용

복호화(Decryption)

암호화 과정에서 사용한 동일한 키로 암호문을 다시 평문으로 변환

과정

평문→암호화 알고리즘→암호문  암호문→복호화 해독키→평문

암호화의 유형

-대칭키 암호화

암호화와 복호화에 동일한 키를 사용

빠르고 효율적, 키를 안전하게 공유하는 것이 어려움

사용예시: 개발팀 환경셋팅, 금고 열쇠, 공용 비밀번호

-비대칭키 암호화

공개키(Public key)와 개인키(Private key)를 사용

공개키로 암호화, 개인키로 복호화 가능

대칭키보다 속도가 느림

-2월 5일-
비트코인의 구조

1. 블록 헤더(Header) - 블록의 메타데이터
2. 트랜젝션 리스트- 블록에 포함된 모든 트랜젝션

-헤더 구조 

크기 80바이트로 고정

주요 구성 요소

- 이전 블록해시 (Previous Block Hash)

이전 블록의 해시 값으로, 블록 간 연결성을 제공

체인형성, 무결성 보장

- 머클 루트 (Merkle Root)

블록 내 모든 트랜젝션을 하나의 해시로 표현

블록 내 모든 트랜잭션이 변경되지 않았음을 증명

- 타임스탬프 (Timestamp)

블록이 생성된 시간

UNX 타임스탬프 형식으로 저장

- 난이도 타겟 (Difficulty Target)

현재 블록 생성 난이도

네트워크의 작업 증명(Proof of Work) 목표를 정의

- 논스 (Nonce)

채굴자가 채굴할 때 변경하는 값(작업증명,poW)

- 버전(Version)

블록이 사용하고 있는 비트코인 프로토콜 버전 정보

-블록 바디 (1MB~4MB)

블록에 포함된 트랜잭션 데이터를 저장

- 코인베이스 트랜잭션 (Coin Transaction)

가장 첫번째 트랙잭션 (채굴자)

블록보상 (채굴보상 + 트랜잭션 수수료)지급을 위한 특별한 트랜잭션

- 일반 트랜잭션 (Transactions)

블록에 포함된 모든 비트코인 전송 기록

트랜잭션의 개수는 네트워크의 상태. 트랜잭션 용량에 따라 달라짐

트랜잭션은 입력(Input), 출력(Output)으로 구성

- 트랜잭션 구조

비트코인이 한 주소에서 다른 주소로 이동하는 데이터 구조

입력, 출력, 수수료로 구성, 각 트랜잭션은 디지털서명을 포함해 보안 유지

- 트랜잭션의 주요 구성 요소
1. 버전 

트랜잭션의 버전

1. 입력

이전 트랜잭션의 출력(UXTO)을 사용하여 새로운 트랜잭션을 생성/ 송신자의 서명이 포함된 정보

-입력 구성요소 

트래잭션 해시( Transaction Hash) 32바이트

현재 트랜잭션이 참조하는 이전 트랜잭션의 해시값

출력 인덱스( Output Index) 4바이트

참조하는 트랜잭션에서 어떤 출력을 사용하는지

지출할 UTXO

스크랩트 길이 (Script Length) 가변

잠금 해제 스크립트의 길이

스크립트 서명 (ScriptSig)

이전 트랜잭션 출력의 소유권을 증명하기 위한 서명과 공개키로 구성된 스크립트

공개키와 디지털 서명이 포함

시퀸스 번호 (Sequence Number) 4바이트

트랜잭션이 취소되거나 수정될 가능성을 나타내는 피드 

현재는 사용 X

1. 출력 (Output)

수신자에게 전딜되는 비트코인의 정보를 포함

한 트랜잭션은 여러개의 출력을 가질 수 있음

-출력 구성요소

출력금액(Value) 8바이트

해당 출력에 포함된 비트코인의 금액

단위: 사토시 ( 1비트코인 = 10^8사토시)

스크립트 길이 (Script Length) 가변

잠금 스크립트의 길이

잠금 스크립트 (Script Length)

비트코인을 잠금(수신자의 주소를 설정)하는 스크립트

일반적으로 P2PKH스크립트 형식 (수신자의 주소를 포함)

트랜잭션 카운터 (Transaction counter) 4바이트

해당 트랜잭션이 유효해지는 조건을 나타냄

- UTXO (Unspent Transaction Output)

사용되지 않은 비트코인의 트랜잭션 출력

비트코인은 계좌기반이 아닌 UTXO모델을 사용하여 코인의 잔액을 추적

사용자가 BTC를 보낼때 기존의 UTXO를 입력으로 사용하여 새로운 트랜잭션을 생성, 남은 잔액을 새로운 UTXO로 변환

- UTXO의 주요 특징

-이중 지불 방지 (Double Spending Prevention)

한 번 사용된 UTXO는 재사용 불가

채굴자는 트랜잭션을 검증할 때, 해당 UTXO가 이전에 사용되지 않았는지 확인

-잔도 개념 필요

기존 화폐처럼 잔돈을 돌려받는 방식

전송이후 잔돈은 새로운 UTXO가 생성 (출력 2개)

-데이터의 투명성과 무결성 유지

블록체인에서 모든 UTXO 공개적으로 조회 가능

사용된 트랜잭션은 더 이상 유효하지 않으므로 데이터 변조 불가

-병령 처리 기능 (Scalability)

각 UTXO는 독립적으로 관리되므로, 여러 개의 트랜잭션을 동시에 처리가능

UTXO의 장점과 단점

-장점

**이중 지불 방지** → 각 UTXO는 한 번만 사용 가능하여 보안성이 높음

**투명성 및 보안성** → 모든 트랜잭션이 블록체인에 기록됨

**병렬 처리 가능** → 독립적인 UTXO 구조 덕분에 병렬 트랜잭션 처리 가능

-단점

복잡한 잔돈관리 → 트랜잭션 처리 시 추가적인 데이터가 필요

저장소 부담 → 전체 네트워크의 UTXO 데이터를 유지하는데 상당한 저장소 필요

- 스크립트 (Script)

UTXO를 소비하기 위해 스크립트 언어를 통해 트랜잭션의 유효성 확인해야되며, 연산자 코드가 그 과정을 담당하게 됨

**UTXO의 소유권 검증**: OP_CHECKSIG와 OP_HASH160을 활용하여 소유자를 확인

**정확한 출력 검증**: OP_EQUAL과 OP_VERIFY를 통해 출력 주소와 금액이 올바른지 확인

**보안성 강화**: OP_DUP과 OP_CHECKMULTISIG로 다중 서명 및 공개 키 변조 방지

- 머클 트리 (Merkle Tree)

트랜잭션 데이터를  계층적으로 해시(hash)하여 저장하는 트리구조

각 트랜잭션을 해시한 후, 상위 노드에서 다시 해시하여 최종적으로 하나의 해시 값(머클루트)을 생성

전체 데이터의 무결성을 간단한 머클 루트 값 하나로 증명 가능

- 머클 트리 생성 과정

**각 트랜잭션 데이터를 해시(SHA-256)하여 리프 노드(Leaf Node) 생성**

**두 개의 해시 값을 결합하여 다시 해시 → 부모 노드 생성**

**이 과정을 반복하여 하나의 최종 해시 값(머클 루트)이 남을 때까지 계속 수행**

- 머클 루트 (Merkle Root)

머클 트리의 최상단(루트) 해시 값, 블록에 포함된 모든 트랜잭션을 대표하는 해시 값

블록 내 모든 트랜잭션의 무결성을 증명하는 역할

- **머클 트리의 주요 기능**

**-데이터 무결성 보장**

머클 루트 값이 변하면 블록 내 트랜잭션이 변경되었음을 의미

블록체인 조작이 불가능하도록 보안 강화

**-빠른 데이터 검증** (머클 프로프, Merkle Proof)

전체 트랜잭션을 다운로드하지 않고도 특정 트랜잭션이 포함되었는지 검증 가능

라이트 노드(SPVs, Simplified Payment Verification)에서 사용됨

**-트랜잭션 데이터 저장 효율성 증가**

개별 트랜잭션 해시만 저장하면 되므로 데이터 저장 공간 절약

**-블록체인 구조 최적화**

모든 트랜잭션을 한 번에 처리하는 것이 아니라 해시값을 활용하여 연산량 감소

2/6

- 중앙 집중형 원장

데이터가 하나의 중앙 기관(은행, 회사, 정부 등)에 의해 관리, 통제되는 방식

- 중앙집중형 원장의 특징

-중앙화된 신뢰: 중앙 기관의 신뢰성과 권위를 기반으로 형성

예: 은행은 거래테이터를 관리, 보증

-단일 장애점 (Single point of failure):

중앙 서버가 해킹, 손상, 장애를 겪으면 데이터가 유실되거나 손상될 위험이 있음

-효율성: 중앙 기관이 데이터를 직접 관리하여 데이터 처리 속도가 빠름

예: 은행 간 정산 시스템

-투명성 부족: 중앙 기관이 데이터를 독점적으로 관리하므로, 참여자는 데이터를 직접 검증하거나 확인할 수 없음

- 분산 원장 (Distributed Ledger)

-중앙 기관 없이 네트워크 참여자들이 데이터를 분산 저장하고, 동기화하며, 관리하는 디지털 원장

-기존의 중앙 집중형 데이터 베이스와 달리, 분산 원장은 여러 노드(컴퓨터)에 동일한 데이터를 복제하여 저장하며, 모든 변경사항이 네트워크 전체에 동기화됨

-데이터의 무결성과 보안 유지

-블록체인은 분산 원장의 한 형태 (블록체인 **≠ 분산원장)**

- 분산 원장의 특징

-분산성: 데이터가 네트워크의 여러 노드에 분산 저장되므로 중앙 서버 불필요

-변경 불가능성: 데이터가 기록된 후 변경 또는 삭제하기 어려움

(데이터의 무결성)

-투명성: 모든 참여자가 동일한 데이터를 볼 수 있어 신뢰 제공

-탈중앙화: 중앙 권한없이 합의를 통해 데이터 추가,수정

- 분산원장의 종류

-퍼블릭 분산원장: 누구나 접근 가능하며, 퍼블릭 블록체인 (예: 비트코인, 이더리움)

-프라이빗 분산원장: 제한된 참여자만 접근 가능, 기업 내부에서 사용 (예: 하이퍼레저)

-컨소시엄 분산원장: 특정그룹 (기업 연합 등) 내에서 공유되며, 참여 노드 제한

- **분산 원장의 활용 사례**

**-금융(Finance)** → 비트코인, 스마트 컨트랙트, 중앙은행 디지털화폐(CBDC)

-**공급망 관리(Supply Chain)** → 제품의 생산부터 유통까지 투명하게 추적

- **헬스케어(Healthcare)** → 의료 기록을 안전하게 관리하고 공유

- **전자 투표(Electronic Voting)** → 조작이 불가능한 온라인 투표 시스템 구축

-**저작권 보호(Digital Rights Management)** → 음악, 영상, NFT 등의 디지털 자산 보호

- 분산 원장 핵심 기슬 (DLT)

-합의 알고리즘: 분산 원장에서 네트워크의 모든 노드가 데이터의 유효성과 순서를 검증하고, 동일한 기록을 유지하기위해 사용하는 방식 (예: poW, poS, PBFT)

-암호화: 데이터의 기밀성, 무결성, 사용자 신원을 인증하기 위해 암호화 기술 사용, 이를 통해 데이터 위변조와 부인을 방지

-노드(Node) 동기화: 모든 노드가 동일한 데이터를 유지하도록 동기화 과정을 거치며, 네트워크의 데이터 일관성, 무결성 보장

- 노드

-분산원장 또는 블록체인 네트워크에서 데이터를 저장, 관리, 다른 노드와 데이터를 교환하는 컴퓨터, 장치

-노드가 많을수록 네트워크가 더욱 탈중항화되고 보안성이 강화됨

-모든 노드는 동일한 데이터를 공유하므로, 일부 노드가 손상되거나 중단되어도 네트워크는 계속 운영됨

- 노드의 역할

**-트랜잭션 검증 (Transaction Validation)** → 새로운 트랜잭션이 유효한지 확인

**-블록 저장 (Block Storage)** → 블록체인 데이터(거래 기록)를 저장

- **네트워크 전파 (Network Propagation)** → 트랜잭션과 블록을 다른 노드에 전송

**-합의 프로세스 참여 (Consensus Participation)** → PoW, PoS 같은 합의 알고리즘 수행

- 노드의 유형

-풀노드 (Full Node):

블록체인의 모든 데이터를 저장하고, 트랜잭션과 블록의 유효성을 독립적으로 검증하는 노드

블록체인의 안전성과 무결성을 유지하는데 핵심적인 역할

예: 비트코인 풀 노드, 이더리움 Geth

-라이트 노드 (Light Node) or SPV 노드(Simple Payment Verification):

블록체인의 전체 데이터를 저장하지 않고, 트랜잭션을 빠르게 검증하는 노드

블록체인의 80바이트 크기의 블록 헤더만 다운로드, 머클루트를 통해 블록 바디 없이도 블록에 포함되었는지 검증 가능

트랜잭션 세부 내열 검증을 위해 풀 노드의 지원 필요

예: 모바일 지갑

-마이닝 노드 (Mining Node):

작업 증명(poW)을 수행하여 새로운 블록을 생성하는 노드

합의 알고리즘에 참여, 블록 보상을 통해 인센티브 

구조적으로 풀 노드와 동일, 비트코인 백서에는 마이닝 노드 키원드 X

예: 비트코인 채굴자, 이더리움 검증자

-검증 노드 (Vaildator Node):

PoS 네트워크에서 블록을 검증하고 합의 과정에 참여하는 노드

에: 이더리움 2.0, 카르다노, 솔라나

-아카이브 노드 (Archive Node):

블록체인의 모든 기록과 상태 데이터를 저장하는 노드

특정 트랜잭션의 과거 기록을 조회하거나 블록체인의 전체 상태를 분석하는데 사용

스마트 컨트랙트가 실행되는 블록체인에 사용

- 비트코인 블록 생성 과정
- 비잔틴 문제(**Byzantine Generals Problem)**

분산 시스템에서 일부 노드가 악의적으로 행동하거나 오류를 일으켜도, 나머지 노드들이 올바른 결정을 내릴 수 있도록 하는 방법을 찾는 것이 핵심

- 비잔틴 장애 허용 (BFT, Byzantine Fault Tolerance)

-네트워크 내 일부 노드가 악의적이거나 오류를 발생시켜도, 나머지 정직한 노드가 올바른 합의에 도달하여 시스템이 정상적으로 작동하도록 보장하는 메커니즘

-모든 분산 노드 체계에선 비잔틴 장애를 해결해야함

-비잔틴 장애: 분산 시스템에서 노드 간의 신뢰 문제가 발생했을 때, 어떻게 모든 정직한 노드가 합의에 도달할 수 있는지를 설명하기 위한 개념

PoW: 작업 증명을 통해 BFT해결

PoS: 지분 증명을 통해 BFT해결

- PoW 작업증명 (Proof of Work)

블록체인 네트워크에서 거래를 검증하고 새로운 블록을 생성하는 합의 알고리즘

poW는 채굴자들이 복잡한 암호학적 연산(해시퍼즐)을 해결해야 블록을 생성할 수 있는 방식

예: 비트코인,이더리움 1.0

- PoW의 핵심개념:

채굴자들이 수학적 퍼즐을 해결하여 블록을 추가하는 방식

**네트워크 보안 유지** → 악의적인 사용자가 블록체인을 조작하기 어렵게 만듦

**경쟁적인 블록 생성** → 많은 채굴자들이 경쟁하여 새로운 블록을 추가

**연산력 기반의 합의 방식** → 더 많은 연산력을 가진 노드가 블록 생성 가능성이 높음

- **PoW의 특징:**

**채굴(Mining)** → 컴퓨터가 연산을 수행하여 해시 퍼즐을 해결

**보안성** → 연산량이 많아질수록 공격이 어려워짐

**속도 문제** → 트랜잭션 처리 속도가 느림(비트코인: 약 10분/블록)

**높은 에너지 소비** → 대량의 전력 사용

- PoW 작동 방식
1. 트랜잭션 생성 

-사용자가 비트코인을 전송하면 네트워크에 트랜잭션 전파

-트랜잭션은 미확인 상태 (메모리 풀, Mempool) 대기

1. 채굴자가 블럭을 생성하기 위해 연산 수행

-채굴자들은 새로운 블록을 추가하기 위해 SHA-256  해시퍼즐을 해결

-이 퍼즐을 푸는 과정이 “작업”

1. 해시 퍼즐 해결 (Nonce 찾기)

-채굴자는 특정 조건을 만족하는 해시 값을 찾기 위해 수많은 조합을 시도

-Nonce를 변경하면서 정답이 나올 때까지 반복연산

1. 정답을 찾은 채굴자가 블록을 추가

-올바른 해시 값을 찾은 채굴자는 새로운 블록을 네트워크에 전파

-다른 노드들이 해당 블록을 검증한 후 블록체인에 추가

1. 채굴자는 보상을 받음

-새로운 블록을 생성한 채굴자는 블록 보상(Block Rewar) + 트랜잭션 수수료(Fee)를 획득

—이 과정을 반복하여 블록체인이 지속적으로 확장됨

- PoW의 장점

-높은 보안성→51% 공격이 어려움

-완전한 탈중앙화 →누구나 채굴에 참여 가능

-이증 지불 방지 → 동일한 코인을 두번 사용불가 (UXTO)

- PoW의 단점

-애너지 소비 문제 → 대량의 전기 사용 (비트코인의 연간 소비 전력= 중소국가)

-확장성 문제 →초당 처리속도가 낮음 (비트코인: 7TPS)

-51% 공격 가능성 → 채굴자들이 연산력의 51% 이상을 장악하면 네트워크 조작 가능

이더리움은 PoW에서 PoS로 전환(하드포크)하여 애너지 문제를 해결하려함

2/8

- 이더리움 (Ethereum

스마트 컨트랟트( Smart Contract)의 분산 애플리케이션(DApp)을 실행할 수있는 확장 가능한 블록체인 플랫폼

창시자: 비탈릭 부테린 

-비트코인에 튜링 안정성을 추가하자 제안

-거절이후 프로그램밍 가능한 블록체인 이더리움 개발

- 이더리움 구조

노드, 트랜잭션 모델, 스마트 컨트랙트, EVM, 합의 알고리즘 등으로 구성

- 이더리움의 핵심 기술

**스마트 컨트랙트** → 블록체인에서 실행되는 자동화된 계약

**EVM (Ethereum Virtual Machine)** → 모든 스마트 컨트랙트를 실행하는 가상 머신

**PoS 합의 알고리즘** → 기존 PoW에서 PoS로 전환하여 확장성과 보안 강화

- 블록체인 모델

이더리움- 어카운트 기반 모델 (Account-based)

모든 사용자와 스마트 계약이 계정으로 표현되며, 계정을 통해 상태(State)와 자산관리

- 계정 종류:

-외부 소유 계정(Externally Owned Account, EOA):

개인이 소유한 계정, 비공개 키에 의해 제어

트랜잭션 생성 가능

-스마트 계약 계정(Contract Account)

특정 코드 (Smart Contract)가 배포된 계정

트랜잭션이 발생하면 해당코드 실행

- 계정 상태

-Nonce: 해당 계정에서 보낸 트랜잭션 수

Balance: 계정에 저장된 이더의 양

Storage: 스마트 계약 데이터(스마트 계약 계정에만 해당)

를 통해 계정 종류 확인 가능

CodeHash: 스마트 계약 코드(스마트 계약 계정 해당)

- 트랜잭션 방식

계정 간에 트랜잭션을 보내 상태 병경

이더를 전송사거나,스마트 계약을 호출하는 트랜잭션

비트코인 VS 이더리움

비트코인: 디지털 화폐

디지털 골드 or p2p 전자화폐의 역할을 목표로 함

중앙 은행 없이 탈중화된 금융 시스템 구축

확장성 및 프로그래밍 기능 제한

이더리움: 탈중앙화된 글로벌 컴퓨터

스마트 컨트랙트를 실행하는 플랫폼

DApp과 DeFi가능

네트워크사의 모든 트랜잭션은 EVM을 통해 실행됨

1. 스마트 계약(Smart Contract)

-블록체인에서 실행되는 자동화된 계약(프로그램)으로, 조건이 충족되면 자동으로 실행되는 코드

-중앙 기관 없이 탈중화된 방식으로 거래, 계약 이행, 데이터 처리가 가능

-이더리움이 최초로 스마트 컨트랙트 기능을 제공, 이후 다양한 블록체인들이 체택

**특징:**

**자동 실행** → 계약 조건이 충족되면 즉시 실행

**변경 불가능(Immutable)** → 배포 후 코드 변경 불가능 (업그레이드는 가능)

**투명성** → 블록체인에 기록되므로 누구나 검증 가능

**보안성** → 중앙 서버 없이 실행되므로 해킹 위험 감소



2/10
- Web

-인터넷 위에서 동작하는 정보 시스템

-웹 브라우저를 통해 사람들이 정보를 검색, 읽기, 쓰기, 상호작용할 수 있는 공간

예: 웹사이트, 블로그, 온라인 포럼

- 인터넷

-물리적인 네트워크 인프라

-전 세계 컴퓨터와 장치들이 서로 연결되어 데이터를 주고받는 기술

예: 이메일, FTP(파일 전송 프로토콜), VoIP(인터넷 전화) 등 다양한 서비스 제공

www 개념

1. 하이퍼텍스트 (링크) 활용

-문서와 문서를 연결하는 링크를 통해 정보를 손쉽게 탐색할 수 있는 방식

-사용자는 특정 문서에서 관련 문서로 이동하며 정보 탐색 가능

1. 인터넷을 활용한 글로벌 정보 공유

-인터넷이라는 네트워크위에서 전 세계 어디서나 정보에 접근하고 공유할 수 있도록 설계

1. 웹의 구성 요소 제안

-HTML(HyperText Markup Language)

역할: 웹 문서의 구조를 정의

예: 제목, 본문, 이미지, 링크 등을 정의하는 태그

중요성: 웹페이지를 구성하는 “뼈대”

-HTTP(HyperText Transfer Protocol)

역할: 클라이언트 (브라우저)와  서버 간에 데이터를 주고받는 프로토콜

작동방식: 사용자가 URL을 입력하면 브라우저가 HTTP요청을 서버로 보내고, 서버는 요청에 대한 데이터를 응답으로 보냄

-URL(Uniform Resource Locator)

역할: 웹 리소스의 위치를 지정하는 주소

예: https://www.naver.com

중요성: 웹페이지, 이미지, 동영상 등 모든 리소스를 고유하게 식별

- W3C (World Wide Web Consortium)

-웹의 표준을 담담하는 기관

<title>웹의 발전 과정</title>

<h1>Web 1.0-정적 웹</h1>

<p><strong>Web 1.0</strong>은 90년대 초 부터 2000년대까지의 시기. 이 시기 웹에서는 사용자가 단순히 <strong>정적인 자료</strong>를 검색해서 데이터를 얻는 <strong>1차원 적인 방식</strong>의 인터넷 환경</p>

<h2>특징</h2>

<li><strong>기간</strong>: 19900년대 초~ 2000년대 초</li>

<li><strong>목적</strong>:목적 제공</li>

<li><strong>기술</strong>:HTML, GIF, CSS (기초적인 스타일링)</li>

<li><strong>구조</strong>:<br>

웹사이트는 정적인 컨텐츠로 구성<br>

사용자는 정보를 읽는 “소비자”역할

<li><strong>상호작용</strong>: 거의 없음 (링크 클릭 정도)</li>

<li><strong>예시</strong>: 초기 야후 디텍토리, 넷스케이프 브라우저</li>

<h2>한계</h2>

사용자는 일방적으로 정보를 제공 받기만 함<br>

컨텐츠 생성은 웹사이트 소유자만 가능

<h1>Web 2.0- 소셜웹</h1>

<p>2000년대 초부터 현재를 의미하는 <strong>Web 2.0</strong>에서는 사용자가 <strong>직접  데이터를 생성</strong>하고 <strong>공유</strong>, Web 2.0부터 전세계의 정보가 폭발적으로 형성. 하지만 이러한 정보의 소유를 플랫폼 기업 등이 독점하게 되면서 사용자 프라이버시 및 데이터 보호의 문제가 대두</p>

<h2>특징</h2>

<li><strong>기간</strong>: 2000년대 초~현재</li>

<li><strong>목적</strong>:사용자 참여와 협업</li>

<li><strong>기술</strong>:AJAX, JavaScript,HTML 5, CSS3</li>

<li><strong>구조</strong>:<br>

사용자가 직접 콘텐츠를 생성하고 공유.<br>

참여형 플랫폼과 소셜 미디어 활성화.</li>

<li><strong>상호작용</strong>:<br>

댓글, 좋아요,  공유 등 사용자의 실시간 참여 기능.<br>

API를 통해 다른 웹사이트와 연결 가능.</li>

<li><strong>예시</strong>:<br>

페이스북, 유튜브, 트위터<br>

위키피디아(협업형 컨텐츠 생성)</li>

<li><strong>장점</strong>:<br>

사용자가 참여로 컨텐츠와 정보가 폭발적으로 증가<br>

인터넷 비즈니스 모델 혁신(광고, 구독 서비스)</li>

<li><strong>한계</strong><br>

데이터 중앙화: 플랫폼 기업(구글, 페이스북 등)이 데이터를 독점<br>

사용자 프라이버시 및 데이터 보호 문제</li>

<h1>Web 3.0-탈중항화의 지능형 웹</h1>

<p>개인화와 지능화에 맞춤형 웹인 <strong>Web 3.0</strong>은 <strong>지능화, 개인화</strong>, 그리고 <strong>탈중앙화</strong>를 중심으로 하는 처세대 웹입니다. 시맨틱 웹 기술과 AI를 활용하여 데이터를 더 잘 이해하고 처리하며, 사용자 맞춤형 정보를 제공. 기존 Web 2.0에서 기업이 데이터를 독점하던 방식에서 벗어나, Web 3.0은 <strong>사용자 데이터 소유권</strong>과 <strong>분산 네트워크</strong>를 통해 새로운 방식의 인터넷 경험을 제공. 블록체인과 스마트 계약을 기반으로 투명성과 보안을 강화하여, NFT와 메타버스와 같은 디지털 생태계와도 통합됨</p>

<h2>특징</h2>

<li><strong>기간</strong>: 현재~미래</li>

<li><strong>목적</strong>: 개인 데이터 소유권 강화, 지능화된 서비스 제공</li>

<li><strong>기술</strong>:<br>

<strong>블록체인</strong>: 데이터의 탈중앙화와 보안<br>

<strong>인공지능(AI)</strong>: 개인화된 경헙 제공<br>

<strong>스마트 계약</strong>: 이더리움과 같은 탈중앙화 애플리켘이션(DApp)<br>

<strong>시맨틱 웹</strong>: 데이터 간 의미 연결로 지능형 정보 검색</li>

<li><strong>구조</strong>:<br>

데이터는 사용자 소유<br>

신뢰 기반 네트워크에서 자동화된 상호작용</li>

<li><strong>상호작용</strong>:<br>

스마트 계약을 통한 자동화된 거래.<br>

NFT와 같은 디지털 자산 소유.</li>

<li><strong>예시</strong>:<br>

이더리움, 디파이(DeFi), NFT 마켓플레이스 (OpenSea)</li>

<li><strong>장점</strong>:<br>

개인 데이터 소유와 보안 강화<br>

데이터 검열 및 독점 문제 해결 가능</li>

<li><strong>한계</strong>:<br>

기술 복잡성으로 인해 대중화까지 시간이 필요<br>

확장성과 네트워크 속도 문제</li>

- www에 대한 개념
1. 하이퍼텍스트 (링크)의 활용
2. 인터넷을 활용한 글로벌 정보 공유
3. 웹의 구성 요소 제안

-HTML (HyperText Markup Language)

-HTTP (HyperText Transfer Protocool)

-URL (Uniform Resource Locator)

-하이퍼텍스트 (Hypertext)

사용자가 텍스트를 읽는 도중에 하이퍼링크를 누르면, 다른 문서로 이동이 가능한 텍스트

-HTML (HyperText Markup Language)

역할:

웹 페이지의 구조와 내용을 작성하는데 사용되는 언어

문서 안에서 텍스트, 이미지, 링크, 표 등을 정의

하이퍼텍스트라는 개념을 통해 다른 문서로 연결(링크) 가능

특징:

태그(tag) 기반 언어.

<html>, <head>, <body>, <a> 등 다양한 태그를 포함

브라우저가 HTML을 렌더링하여 사용자에게 시각적으로 웹페이지를 표시

-HTTP

역할:

클라이언트 (웹 브라우저)와 서버 간의 통신 규칙을 정의하는 프로토콜.

웹 페이지와 관련된 리소스를 요청하고 응답을 받는 방식 제공.

특징:

요청(request)과 응답(response) 구조.

요청 메서드: GET, POST, PUT, DELETE 등.

상태 코드: 200(성공), 404(자원 없음), 500(서버 오류) 등.

동장방식:

A. 클라이언트가 서버에 요청을 보냄.

B. 서버가 요청을  처리하고 결과를 응답.

C. 브라우저가 응답 내용을 해석해 사용자에게 보여줌.

-URL (Uniform Resource Locator)

역할:

웹 상의 리소스(문서, 이미지, 동영상 등)를 고유하게 식별하기 위한 주소 체계.

사용자가 원하는 정보를 찾을 수 있도록 서버와 리소스를 지정.

구조:

일반적인 URL형식: 프로토콜://도메인/경로?쿼리문자열#프래그먼트

예: https://www.example.com/page?id=123#section

구성요소:

-프로토콜: 데이터를 주고받는 방식 (예 http, https)

-도메인: 서버 주소 또는 IP 주소(예:www.example.com)

-경로: 서버 내에서 자원의 위치(예: /page)

-쿼리 문자여리 추가적인 요청 정보 (예: #section)

- 웹 기술 발전 이후 추가된 요소

-클라이언트(Client)

역할:

클라이언트는 사용자가 서버와 상호작용하기 위한 장치나 소프트웨어를 의미

서버에 요청(Request)을 보내고 응답(Response)을 받아 처리하여 사용자에게 데이터를 표시

웹 브라우저 (Chrome, Firefox, Edge 등)는 대표적인 크라이언트 애플리케이션

특징:

사용자 중심 인터페이스: 사용자가 서버 데이터를 시각적으로 확인하거나 입력할 수 있는 환경을 제공

요청(Request) 생성: 사용자가 웹 브라우저에 URL을 입력하면 HTTP/HTTPS 프로토콜을 통해 서버에 데이터를 요청

응답 (Response)처리: 서버로부터 받은 HTML, CSS, JavaScript 등을 렌더링하여 사용자 화면에 표시.

캐시 (Cache) 기능: 이전에 받은 데이터를 저장하여 성능을 향상시키고 네트워크 요청을 줄임.

동적 동작 지원: JavaScript와 같은 기술을 통해 서버와의 추가적인 통신 없이도 페이지를 동적으로 업데이트

동작:

사용자가 버튼을 크릭하면 fatch 함수를 통해 서버에서 데이터를 요청

서버 응답 데이터를 받아 <p id=”output”> 에 표시

주요 클라이어트 소프트웨어:

웹 브라우저: Chrome, Firefox, Safari, Edge.

모바일 애플리케이션: iOS 및 Android용 앱.

-서버(Server)

역할:

서버는 클라이언트로부터 요청→처리→적절한 데이터를 응답하는 역할

데이터, 리소스 저장/ 클라이언트 요청에 따라 제공, 처리

웹사이트, 애플리케이션, 데이터베이스 등의 동작을 지원하는 증심 역할 수행

특징:

항상 대기 상태: 클라이언트 요청에 응답하기 위해 항상 실행중

데이터 저장 및 관리: HTML, CSS, JavaScript 파일, 이미지, 데이터베이스 등 다양한 리소스 저장

다양한 처리 능력: 

정적 컨텐츠 제공(HTML, CSS등)

동적 컨텐츠 생성 (API 호출, 데이터베이스 처리 등)

확장성: 트래픽 증가에 따라 여러 서버를 연결 (로드 밸런싱)하거나 클라우드 서비스로 확장 가능

보안: HTTPS를 통해 클라이언트와 데이터를 암호화하여 안전하게 통신

동작:

클라이언트가 http://localhost:3000/ 으로 요청하면 서버가 <h1>Welcome to the Server</h1>을 반환

다른 URL 요청 시 404 Not Found 응답

- 서버의 종류

-웹 서버 (Web Server)

HTTP 요청을 처리하고 HTML,CSS, 이미지 등을 클라이언트에 제공

주로, 배포 단계에서 사용

예: Apache, Nignx

-애플리케이션 서버 (Application Server)

동적 요청 처리 (예: 데이터베이스와 상호작용, API호출)

주로, 서비스 로직 개발에서 사용

예: Node.js, Spring Boot

-데이터베이스 서버 (Database Server)

데이터 저장 및 관리를 전담

예: MySQL, PosrgreSQL, MongoDB

-파일 서버 (File Server)

클라이언트에 파일을 저장하고 전송

근래, Amazon S3, Google Cloud Storage, Microsoft Azure Blob Storage 등 클라우드 기반 파일 서버

예: FTP 서버

-서버 실제 사용 예:

정적 웹 페이지 제공: 단순한 HTML 파일 제공

동적 컨텐츠 처리: 사용자의 로그인 요청 처리, 검색 결과 반환

API 제공: REST 또는 GraphQL API를 통해 데이터 전달 

- 웹페이지를 구성하는 3가지 핵심요소

-HTML (HyperText Markup Language)

역할:

웹페이지의 구조와 내용을 작성하는데 사용되는 언어

문서 안에서 텍스트, 이미지, 링크, 표 등을 정의

하이퍼텍스트(hypertext)라는 개념을 통해 다른 문서로 연결(링크) 가능

특징:

태그(tag) 기반 언어

<html>,<head>,<body>,<a> 등 다양한 태그를 포함

브라우저가 HTML을 렌더링하여 사용자에게 시각적으로 웹페이지를 표시

-CSS (Cascading Style Sheets)

역할:

웹페이지의 디자인과 레이아웃을 담당하는 언어

HTML로 작성된 구조에 스타일을 적용하여 색상, 글꼴, 여백, 배경 등을 꾸밈

사용자가 보다 시각적으로 보기 좋은 페이지를 경험할 수있도록 만듬

특징:

HTML과 분리된 외부 스타일시트 (.css 파일)로 관리 가능

선택자(selector)를 사용하여 특정 HTML 요소에 스타일 적용

반응형 디자인을 지원하여 다양한 기기에 적합한 레이아웃 제공.

-JavaScript

역할: 

웹 페이지에 동적 기능을 추가하는 프로그래밍 언어

버튼 클릭, 입력 폼 검증, 데이터 로드, 애니메이션 등 인터랙션을 담당

HTML과 CSS로 만든 페이지를 더욱 생동감 있고 유용하게 만듬

특징:

클라이언트 측에서 동작(브라우저)

HTML과 CSS에 동적인 행동 추가

다양한 라이브러리 및 프레임워크와 함께 사용 가능


2/12

- HTML (HyperText Markup Language, 하이퍼텍스트 마크업 언어)

-웹페이지를 구성하는 기본 언어, 텍스트를 구조화하고  멀티미디어 요소를 포함하며 브라우저가 컨텐츠를 표시하는 방식을 정의

-웹페이지의 뼈대를 구성하는 마크업 언어

-HTML문서는 다른 개발자가 일고 수정할 가능성이 있으므로, 의미있는(Semantic) 태그를 적절히 활용하면 문서의 가독성과 협업 효율성이 크게 향상됨

 

- HTML의 특징
1. 하이퍼 텍스트( HyperText)
    
    문서 간 연결(링크)을 의미
    
    HTML의 <a> 태그를 사용하여 웹페이지 간의 하이퍼링크 생성
    
    예: <a href=”https://google.com”> 구글로 이동 </a>
    
2. 마크업 언어 (Markup Language)
    
    텍스트에 태그(tag, <….>)를 추가하여 구조와 의미를 정의하는 언어
    
    예: <h1> 은 제목 <p>는 단락
    
    <h1>제목입니다.</h1>
    
    <p>이것은 단락입니다.</p>
    
3. 브라우저에서 해석
    
    HTML파일은 웹브라운저가 읽고 해석하여 사용자에게 웹페이지로 렌더링
    
    예: HTML 코드는 브라우저에서 시각적인 컨텐츠로 변환
    

- HTML의 기본구조

예:

<!DOCTYPE html>

<html>

<head>

<title>웹페이지의 제목</title>

</head>

<body>

<h1>가장 큰 제목</h1>

<p>단락을 나누는 단어</p>

</body>

</html>

구성요소 

1. <!DOCTYPE html>
    
    HTML5 문서를 선언하는 코드
    
    브라우저가 HTML5 규격애 맞게 컨텐츠를 해석하도록 지정 
    
2. <html>
    
    HTML 문서의 루트(root) 요소로, 모든 HTML 태그를 감쌈
    
3. <head>
    
    문서의 메타정보를 담는 부분
    
    <title> 태그: 브라우저 탭에 표시되는 제목
    
    <meta> 태그: 문서 정보(인코딩, 뷰포트 등)를 설정
    
4. <body>
    
    사용자가 실제로 볼 수 있는 컨텐츠를 담는 부분
    
    텍스트, 이미지, 링크, 폼 등 다양한 요소가 포함
    
    <h1> ~ <h6> heading을 의미, 크기에 따라 h1~h6
    
    <p> 단락태그, 문장을 단락으로 표시
    
    <br> 줄바꿈 태그
    
    <hr> 수평선 태그, 문단을 구분하는 선
    
    <div> content division을 의미, 줄바꿈됨
    
    <span> 쥴바꿈이 없는 content 컨테이너
    
    href : 링크의 대상 URL
    
    src: 이미지 파일 경로
    
    alt: 이미지를 대체하는 텍스트 (접근성을 위한 설명)
    
    <li> 목록 태그 (리스트)
    
    <ol> 순서있는 리스트: 번호로 구성된 리스트
    
    <ul> 순서없는 리스트: 점으로 구성된 리스트
    

</태그이름>은 해당 태그가 끝났음을 의미

- HTML 속성(Attribute)은 태그 에 추가 정보를 제공하여 해당 요소의 동작이나 스타일을 설정하는데 사용

속성은 항상 시작 태그 안에 작성되며, 속성명=”값”의 형식으로 표현

- 속성의 기본 형식

<태그 속성명=”값’>내용</태그>

속성명: 속성의 이름을 정의

값: 속성의 동작이나 설정을 지정

속성과 값은 공백 없이 등호 (=)로 연결되며, 값은 큰따옴표(”)로 묶는 것이 표준

- HTML 속성의 주요 특징
    1. 모든 태그에 적용 가능
    
    속성은 특정 태그의 동작을 정의하거나 스타일을 적용할 때 사용
    
    1. 공백없이 작성
    
    속성명과 값 사이에 공백이 있으면 오류 발생
    
    1. 다중 속성 사용 가능
    
    하나의 태그에 여러개의 속성 사용가능 
    

- 속성의 중요성
    1. 요소의 동작 설정 
    
    태그에 필요한 동작이나 정보를 제공, 요소를 제대로 작동하게 함
    
    1. CSS 및 JavaScript와 연동
    
    id 와 class 속성은 스타일 지정(CSS)과 동적 동작(JavaScript) 구현의 핵심
    
    1. 접근성과 SEO 향상
    
    alt 와 title 속성은 웹 접근성과 검색 엔진 최적화(SEO)에 도움을 줌
    

- 자주 사용하는 속성
    1. id 와 class
        
        
        id: HTML 요소에 고유한 식별자 부여
        
        예: <h1  id=”main-title”>제목</h1>
        
        class: HTML 요소를 그룹화하여 CSS나 JavaScript에서 스타일 및 동작을 적용
        
        예: <p class=”highlight”>강조된 텍스트</p>
        
    
    1. href (하이퍼링크)
        
        <a> 태그에서 링크의 URL을 지정
        
        예: <a href=”https://example.com”>Example 사이트로 이동</a>
        
    
    1. src (이미지 및 리소스 경로)
        
        리소스(이미지, 비디오 등)의 경로를 지정
        
        예: <img src=”image.jpg” alt=”이미지 설명”>
        
    
    1. alt (대체 택스트)
        
        이미지가 로드되지 않을 때 표시되는 텍스트로, 접근성을 향상
        
        예:<img src=”image.jpg” alt=”이미지 설명”>
        
    
    1. style (인라인 스타일)
        
        특정 태그에 CSS 스타일을 직접 적용
        
        예:<p style=”color: red; font-size: 18ppx;”>빨간 텍스트 </p>
        
    
    1. title
        
        요소에 툴팁(마우스를 올렸을 때 나타나는 텍스트)추가
        
        <a href=”https://example.com” title=”예제 사이트”>Example</a>
        
    
    1. 폼 관련 속성
        
        <input> 과 같은 폼 태그에서 자주 사용
        
        type: 입력 필드의 유형 지정 (예: text, password, email)
        
        placeholder: 입력 필드에 힌트를 제공
        
        required: 필수 입력 필드 지정
        
        예: <input type=”email” placeholder=”이메일을 입력하세요” required>
        
    
    1. 그외 HTML5 추가속성 
        
        data-*: 사용자 정의 데이터를 저장하는 커스텀 속성
        
        예: <div data-id=”12345”>데이터 속성</div>
        
        미디어 관련 속성
        
        controls, autoplay, loop: <audio> 및 <video> 태그의 속성
        
        예: <video src=”video.mp4” controls autoplay loop></video>
        
- SEO (Search Engine Optimization)

SEO(검색 엔진 최적화)는 검색엔진에서 웹사이트가 더 높은 순위에 노출되도록 최적화하는 작업

검색 엔진은 특정 키워드에 대해 관련성 높은 컨텐츠를 사용자에게 제공하기 위해 웹페이지를 색인(index)하고 분석

SEO는 이 과정을 이해하고, 웹사이트가 검색 결과에서 상위에 표시되도록 조정하는 전략

- SEO에 중요한 HTML태그

1. <title> 태그
    
    페이지의 제목을 정의, 검색 엔진 결과 페이지 (SERP)에 표시
    
    각 페이지마다 고유하고 명확한 제목을 작성
    
    예: <title>효과적인 SEO를 위한 HTML 태그 설명</title>
    
    -검색 결과에서의 역할:
    
    <title> 태그의 내용은 링크로 표시
    

1. <meta> 태그
    
    2-1 <meta name=”description”> 
    
    페이지의 요약 정보를 제공, 검색 결과에서 링크 아래에 표시
    
    예: <meta name=”description” content=”HTML에서 SEO에 유용한 태그에 대해 배우고 검색 순위를 높이는 방법을 학습하세요.”>
    
    2-2 <meta name=”keywords”>
    
    페이지와 관련된 키워드를 나열/ 현재는 검색엔진에서 거의 사용되지 않음
    
    예: <meta name=”keywords” content=”HTML, SEO, 태그, 검색 엔진 최적화”>
    
    2-3 <meta name=”robots”>
    
    검색 엔진 크롤러에 페이지 크롤링 또는 색인 여부를 지시
    
    예: <meta name=”robot” content=”index, follow”>
    
    옵션:
    
    index: 검색 엔진이 페이지를 색인
    
    noindex: 색인하지 않음
    
    follow: 링크를 따라감
    
    nofollow: 링크를 따라가지 않음
    
2. 시맨틱 태그 (Semantic Tags)
    
    페이지 구조와 컨텐츠의 의미를 명확히 전달하여 검색엔진이 페이지를 쉽게 분석할 수 있도록 도움
    
    주요 시맨틱 태그:
    
    <header>: 페이지 또는 섹션의 헤더
    
    <nav>: 내비게이션 메뉴
    
    <main>: 주요 컨텐츠 영역
    
    <article>: 독립적인 컨텐츠
    
    <section>: 관련된 컨텐츠 그룹
    
    <footer>: 페이지 또는 섹션의 푸터
    

1. <h1> ~ <h6> 태그
    
    제목태그는 컨테츠의 계층 구조 <h1>은 페이지의 가장 중요한 제목
    
    각 페이지에 하나의 <h1>태그만 사용하는 것이 좋음
    

1. <a> 태그와 앵커 텍스트
    
    링크를 통해 다른 페이지로 연결
    
    페이지의 주제를 설명, 검색엔진이 링크 목적을 이해하는데 도움
    
2. 이미지 태그와 대체 텍스트 (All Text)
    
    <img>태그의 alt 속성은 이미지의 대체 텍스트를 제공, 이미지가 로드되지 않을떄 표시
    
    alt 텍스트는 검섹 엔진이 이미지의 내용을 이해하는데 도움
    

1. URL 구조와 <link> 태그
    
    URL
    
    간결하고 키워드를 포함한 URL은 검섹 엔진 최적화에 유리
    
    예: https://example.com/seo-html-tags
    
    Canoncial 태그:
    
    동일한 컨텐츠가 여러 URL에 존재할 경우 기본 URL을 지정
    
    예: <link rel=”cananical” href=”https://example.com/seo-html-tags”>
    

- SEO 태그 사용의 중요성
    1. 검색엔진에 정보 제공: 페이지의 주제, 구조, 목적을 검색 엔진에 명확히 전달
    2. 검색 순위 향상: 적절한 태그와 키워드 최적화는 검색 결과에서 상위에 노출될 가능성을 높임
    3. 사용자 경험 개선: 잘 작성된 SEO태그는 사용자가 검색결과를 통해 페이지의 내용을 이해하는데 도움을 줌
 

 
2/19
JavaScript 


- DOM (Document Object Model) 문서 객체 모델

HTML(웹페이지)를 JS에서 조작할 수 있도록 만든 구조

- DOM의 기본 개념
1.  DOM의 트리 구조
<!DOCTYPE html>
<html>
<head>
    <title>My Page</title>
</head>
<body>
    <h1 id="title">Hello, World!</h1>
    <button>Click Me</button>
</body>
</html>

Document
 ├── html
 │   ├── head
 │   │   └── title (My Page)
 │   ├── body
 │   │   ├── h1#title (Hello, World!)
 │   │   └── button (Click Me)

----
