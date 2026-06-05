# 📘 배달의민족 데이터 카탈로그 (전체 테이블)

> 이 문서는 AI 코딩 어시스턴트(Claude Code, Cursor 등)에 입력하기 최적화된 마크다운 형식의 데이터 사전입니다.
> 각 테이블의 스키마, 중요도, 컬럼 정보 및 비즈니스 설명을 모두 포함하고 있습니다.

## 📁 Schema: `sborder`

### 📄 Table: `ad_campaign`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `uuid` | `varchar` | - |
| 2 | `created_date` | `timestamp(9)` | - |
| 2 | `modified_date` | `timestamp(9)` | - |
| 2 | `created_by` | `varchar` | - |
| 2 | `modified_by` | `varchar` | - |
| 2 | `order_no` | `varchar` | - |
| 2 | `ad_kind_id` | `varchar` | - |
| 2 | `ad_kind_key` | `varchar` | 수수료율  정책 |
| 2 | `ad_campaign_id` | `varchar` | 수수료율 |
| 2 | `commission_rate_policy` | `varchar` | 수수료율  할인 |
| 2 | `commission_rate_value` | `double` | 적용된  수수료율  할인 정책들  (`,` 로 구분) |
| 2 | `commission_rate_discount` | `double` | 배달비  정책 |
| 2 | `commission_discount_policies` | `varchar` | 배달비 |
| 2 | `delivery_supply_price_policy` | `varchar` | 배달비  할인 |
| 2 | `delivery_supply_price_value` | `bigint` | 적용된  배달비  할인 정책들  (`,` 로 구분) |
| 2 | `delivery_supply_price_discount` | `bigint` | - |
| 2 | `delivery_discount_policies` | `varchar` | - |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |
| 2 | `uuid` | `varchar` | - |
| 2 | `created_date` | `timestamp(9)` | - |
| 2 | `modified_date` | `timestamp(9)` | - |
| 2 | `created_by` | `varchar` | - |
| 2 | `modified_by` | `varchar` | - |
| 2 | `order_no` | `varchar` | - |
| 2 | `ad_kind_id` | `varchar` | - |
| 2 | `ad_kind_key` | `varchar` | - |
| 2 | `ad_campaign_id` | `varchar` | - |
| 2 | `commission_rate_policy` | `varchar` | 수수료율  정책 |
| 2 | `commission_rate_value` | `double` | 수수료율 |
| 2 | `commission_rate_discount` | `double` | 수수료율  할인 |
| 2 | `commission_discount_policies` | `varchar` | 적용된  수수료율  할인 정책들  (`,` 로 구분) |
| 2 | `delivery_supply_price_policy` | `varchar` | 배달비  정책 |
| 2 | `delivery_supply_price_value` | `bigint` | 배달비 |
| 2 | `delivery_supply_price_discount` | `bigint` | 배달비  할인 |
| 2 | `delivery_discount_policies` | `varchar` | 적용된  배달비  할인 정책들  (`,` 로 구분) |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `charge_line`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `uuid` | `varchar` | - |
| 1 | `created_date` | `timestamp(9)` | - |
| 1 | `modified_date` | `timestamp(9)` | - |
| 1 | `created_by` | `varchar` | - |
| 1 | `modified_by` | `varchar` | - |
| 1 | `amount` | `bigint` | - |
| 1 | `charge_type` | `varchar` | - |
| 1 | `order_uuid` | `varchar` | ?? ??? |
| 1 | `seller_charge_amount` | `bigint` | 배달팁  할인 우형 부담금 |
| 1 | `takeout_discount_rate` | `integer` | 기본 배달팁  할인 멤버쉽  부담금 |
| 1 | `woowabros_charge_amount` | `bigint` | 추가거리  배달팁  할인 멤버쉽  부담금 |
| 1 | `membership_base_charge_amount` | `bigint` | MFO 배달팁  할인금액 |
| 1 | `membership_extra_distance_charge_amount` | `bigint` | 배달팁  할인 HVA 부담금 |
| 1 | `mfo_charge_amount` | `bigint` | 배달팁  원금액 |
| 1 | `hva_charge_amount` | `bigint` | - |
| 1 | `origin_amount` | `bigint` | - |
| 1 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `coupon_line`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `part_date` | `string` | - |
| 2 | `uuid` | `varchar` | - |
| 2 | `created_date` | `timestamp(9)` | - |
| 2 | `modified_date` | `timestamp(9)` | - |
| 2 | `created_by` | `varchar` | - |
| 2 | `modified_by` | `varchar` | - |
| 2 | `amount` | `bigint` | - |
| 2 | `calculate_type_code` | `varchar` | - |
| 2 | `coupon_code` | `varchar` | - |
| 2 | `coupon_name` | `varchar` | - |
| 2 | `coupon_seq` | `bigint` | - |
| 2 | `order_no` | `varchar` | - |
| 2 | `seller_charge_amount` | `bigint` | - |
| 2 | `coupon_token` | `varchar` | - |
| 2 | `cpn_grp_seq` | `integer` | - |
| 2 | `cpn_mem_seq` | `bigint` | 쿠폰멤버순번 ( 신규 쿠폰Id) 쿠폰시스템  기준 키 |
| 2 | `coupon_member_no` | `varchar` | 쿠폰 소유자  회원 번호 |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `delivery`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `uuid` | `varchar` | - |
| 1 | `created_date` | `timestamp(9)` | - |
| 1 | `modified_date` | `timestamp(9)` | - |
| 1 | `created_by` | `varchar` | - |
| 1 | `modified_by` | `varchar` | - |
| 1 | `detail` | `varchar` | - |
| 1 | `dong` | `varchar` | - |
| 1 | `old_address` | `varchar` | - |
| 1 | `old_street_name_address` | `varchar` | - |
| 1 | `sido` | `varchar` | - |
| 1 | `sigungu` | `varchar` | - |
| 1 | `cook_time_minutes` | `integer` | - |
| 1 | `delivery_time_minutes` | `integer` | - |
| 1 | `delivery_type` | `varchar` | - |
| 1 | `latitude` | `varchar` | - |
| 1 | `longitude` | `varchar` | - |
| 1 | `is_reservation` | `tinyint` | - |
| 1 | `reservation_datetime` | `timestamp(9)` | - |
| 1 | `rgn3` | `varchar` | - |
| 1 | `recipient_phone_number` | `varchar` | - |
| 1 | `delivery_datetime` | `timestamp(9)` | - |
| 1 | `delivery_agency_type` | `varchar` | - |
| 1 | `receipt_number` | `varchar` | - |
| 1 | `table_number` | `varchar` | - |
| 1 | `table_display_name` | `varchar` | - |
| 1 | `delivery_option_type` | `varchar` | 배달옵션 (2023-12-05 추가) |
| 1 | `delivery_carry_type` | `varchar` | 배달방식  타입(2023-12-05 추가) |
| 1 | `assigned_delivery_carry_type` | `varchar` | 탄력 배달 발생시  지정된  배달방식 |
| 1 | `add_cook_time_minutes` | `integer` | 추가 조리 시간 (n 분) |
| 1 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `instant_discount_line`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `uuid` | `varchar` | uuid |
| 2 | `order_no` | `varchar` | 주문번호 |
| 2 | `discount_id` | `varchar` | 즉시할인  아이디 |
| 2 | `bucket_type` | `varchar` | 즉시할인  대분류  (ORDER / DELIVERY) |
| 2 | `discount_policy_code` | `varchar` | 즉시할인  유형 |
| 2 | `amount` | `bigint` | 즉시할인  금액 |
| 2 | `distributions` | `varchar` | 분담금 |
| 2 | `cofunding_id` | `varchar` | 코펀딩  id |
| 2 | `is_baemin_club_discount` | `tinyint` | 배민클럽  할인 여부 |
| 2 | `created_date` | `timestamp(9)` | 생성일시 |
| 2 | `modified_date` | `timestamp(9)` | 수정일시 |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `line_item_discount`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 5 | `uuid` | `varchar` | - |
| 5 | `created_date` | `timestamp(9)` | - |
| 5 | `modified_date` | `timestamp(9)` | - |
| 5 | `created_by` | `varchar` | - |
| 5 | `modified_by` | `varchar` | - |
| 5 | `discount_amount` | `bigint` | - |
| 5 | `line_item_uuid` | `varchar` | - |
| 5 | `discount_mapping_id` | `varchar` | - |
| 5 | `type` | `varchar` | - |
| 5 | `option_group_id` | `varchar` | 옵션그룹아이디 |
| 5 | `option_mapping_id` | `varchar` | 옵션아이디 |
| 5 | `distributions` | `varchar` | 분담금 |
| 5 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `order_cancel_demand`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 3 | `uuid` | `varchar` | uuid |
| 3 | `created_date` | `timestamp(9)` | 생성일시 |
| 3 | `modified_date` | `timestamp(9)` | 수정일시 |
| 3 | `order_no` | `varchar` | 주문번호 |
| 3 | `reason` | `varchar` | 주문취소요청사유 |
| 3 | `status` | `varchar` | 주문취소요청상태 |
| 3 | `created_date_time` | `timestamp(9)` | 주문취소요청일시 |
| 3 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `order`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 5 | `uuid` | `varchar` | uuid |
| 5 | `created_date` | `timestamp(9)` | 생성일시 |
| 5 | `modified_date` | `timestamp(9)` | 수정일시 |
| 5 | `created_by` | `varchar` | 생성자 |
| 5 | `modified_by` | `varchar` | 수정자 |
| 5 | `accept_datetime` | `timestamp(9)` | 접수일시 |
| 5 | `cancel_datetime` | `timestamp(9)` | 취소일시 |
| 5 | `contract_type` | `varchar` | 계약타입 ( 정산) |
| 5 | `delivery_uuid` | `varchar` | 배송 참조키 (FK) |
| 5 | `member_no` | `varchar` | 회원번호 |
| 5 | `order_datetime` | `timestamp(9)` | 주문일시 |
| 5 | `order_no` | `varchar` | 주문번호 |
| 5 | `order_status` | `varchar` | 주문상태 |
| 5 | `orderer_tel` | `varchar` | 주문자  연락자 |
| 5 | `purchase_type` | `varchar` | 구매방식 |
| 5 | `reason_code` | `varchar` | 변경사유코드 |
| 5 | `seller_summary_uuid` | `varchar` | 판매자  참조키 (FK) |
| 5 | `service_channel` | `varchar` | 서비스채널 |
| 5 | `service_type` | `varchar` | 서비스타입 [ 배민, 배라] |
| 5 | `shop_no` | `varchar` | 가게번호 |
| 5 | `shop_owner_no` | `varchar` | 가게업주번호 |
| 5 | `tx_amount` | `bigint` | 거래금액 ( 빌링) |
| 5 | `dsm_no` | `varchar` | dsm 번호 |
| 5 | `order_type` | `varchar` | 주문 방식 |
| 5 | `shop_number` | `varchar` | 신규 가게 번호 |
| 5 | `division_version` | `varchar` | 안분계산기  버전 |
| 5 | `soldout_policy_type` | `varchar` | 품절 정책 타입 |
| 5 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `line_item`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 5 | `uuid` | `varchar` | - |
| 5 | `created_date` | `timestamp(9)` | - |
| 5 | `modified_date` | `timestamp(9)` | - |
| 5 | `created_by` | `varchar` | - |
| 5 | `modified_by` | `varchar` | - |
| 5 | `item_description` | `varchar` | - |
| 5 | `item_mapping_id` | `varchar` | - |
| 5 | `item_name` | `varchar` | - |
| 5 | `item_type` | `varchar` | - |
| 5 | `order_uuid` | `varchar` | - |
| 5 | `price` | `bigint` | - |
| 5 | `quantity` | `integer` | - |
| 5 | `sort_number` | `integer` | - |
| 5 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `order_status_history`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `id` | `varchar` | 식별자 |
| 1 | `member_id` | `varchar` | member 테이블의  식별자 |
| 1 | `membership_code` | `varchar` | 상품 코드 |
| 1 | `promotion_group_types` | `varchar` | 지급 받은 프로모션  그룹 |
| 1 | `start_date_time` | `timestamp(9)` | 구독 시작일 |
| 1 | `end_date` | `date` | 구독 종료일 |
| 1 | `recurrent_number` | `varchar` | 정기결제  번호 |
| 1 | `created_datetime` | `timestamp(9)` | 데이터  생성 일시 |
| 1 | `modified_datetime` | `timestamp(9)` | 데이터  수정 일시 |
| 1 | `region` | `varchar` | 구독 지역 코드 ( 법정동 ) |
| 1 | `next_payment_date` | `date` | 다음 유료 결제일 |
| 1 | `group_key` | `varchar` | 멤버십  회차 그룹 키 |
| 1 | `part_date` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `sborder_mart`

### 📄 Table: `order_master`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 5 | `ord_no` | `varchar` | 주문번호 |
| 5 | `service_type` | `varchar` | 서비스타입 |
| 5 | `delivery_type` | `varchar` | 배달타입 |
| 5 | `service_channel` | `varchar` | 서비스채널타입 |
| 5 | `mem_no` | `varchar` | 회원번호 |
| 5 | `dvc_id` | `varchar` | 디바이스아이디 |
| 5 | `shop_no` | `varchar` | 업소번호 |
| 5 | `shop_category` | `varchar` | 업소카테고리 |
| 5 | `ord_referrer` | `varchar` | 주문경로 |
| 5 | `order_status` | `varchar` | 주문상태 |
| 5 | `reason_code` | `varchar` | 사유코드  코드 값은 아래 문서의  내용으로  확인 가능합니다 . (https://docs.google.com/spreadsheets/d/1zv4GfnWG7doH6Sl844x6a-U0KIuw3Ha3n1HVdMWRhnU/edit |
| 5 | `pay_method` | `varchar` | 주결제수단 |
| 5 | `ord_price` | `bigint` | 주문금액 |
| 5 | `delivery_tip` | `bigint` | 배달팁 |
| 5 | `coupon_discount` | `bigint` | 쿠폰할인금액 |
| 5 | `takeout_discount` | `bigint` | 포장할인금액  (F/O - 2025-07-22) |
| 5 | `takeout_discount_rate` | `double` | 포장할인비율  (F/O - 2025-07-22) |
| 5 | `employee_discount` | `bigint` | 직원할인 |
| 5 | `ad_campaign_id` | `varchar` | 광고상품 ID |
| 5 | `ad_inventory_key` | `varchar` | 광고인벤토리 Key |
| 5 | `order_accept_channel` | `varchar` | 주문접수채널 |
| 5 | `site_no` | `varchar` | 사이트 |
| 5 | `delivery_agency_id` | `varchar` | ( 배라) 센터번호 |
| 5 | `delivery_agency_type` | `varchar` | 배달대행타입 |
| 5 | `notified_time_minutes` | `integer` | 알림톡안내  소요시간 |
| 5 | `delivery_time_minutes` | `integer` | 배달 소요시간 |
| 5 | `seller_charge_amount` | `bigint` | 업주부담금 |
| 5 | `delivery_commission` | `bigint` | 배달커미션  금액 |
| 5 | `delivery_commission_rate` | `double` | 배달커미션  비율 |
| 5 | `is_test` | `tinyint` | 테스트주문  여부 |
| 5 | `is_member` | `tinyint` | 회원주문  여부 |
| 5 | `is_closed` | `tinyint` | 완료주문  여부 |
| 5 | `is_reservation` | `tinyint` | 예약주문  여부 |
| 5 | `rgn1_cd` | `varchar` | 지역1 코드 ( 법정동  전환 기간 : 2018-10-19~) |
| 5 | `rgn2_cd` | `varchar` | 지역2 코드 ( 법정동  전환 기간 : 2018-10-19~) |
| 5 | `rgn3_cd` | `varchar` | 지역3 코드 ( 법정동  전환 기간 : 2018-10-19~) |
| 5 | `order_date` | `timestamp(9)` | 주문일시 |
| 5 | `small_order_fee` | `integer` | 소액주문비  금액. 2021.04.23 배민1 관련 추가 컬럼으로  배민1 주문의  경우에만  값이 유효합니다 . ( 이외 inventory_key 는 값이 모두 0 ) |
| 5 | `extra_delivery_tip` | `integer` | 거리초과  할증 배달팁 . 2021.04.23 배민1 관련 추가 컬럼으로  배민1 주문의  경우에만  값이 유효합니다 . ( 이외 inventory_key 는 값이 모두 0 ) |
| 5 | `seller_charge_coupon_discount` | `bigint` | 업주부담쿠폰할인금액 |
| 5 | `menu_discount` | `bigint` | 메뉴할인금액 |
| 5 | `gift_amount` | `bigint` | 상품권사용금액 |
| 5 | `point_amount` | `bigint` | 포인트사용금액 |
| 5 | `baemin_point_amount` | `bigint` | 배민포인트사용금액 |
| 5 | `os_cd` | `varchar` | 앱 OS 구분1: iOS, 2: 안드로이드 , 0: 그 외 |
| 5 | `app_ver` | `varchar` | 앱 버젼 입력예시 : 6.12.1 |
| 5 | `gender` | `varchar` | 구매 시점의  성별 |
| 5 | `age` | `integer` | 구매 시점의  나이 |
| 5 | `is_group_order` | `tinyint` | 함께주문  여부 |
| 5 | `is_stod` | `tinyint` | 알뜰배달  주문 여부. 배민1 일반( 묶음) 배달 서비스를  제공하는  상품 주문의  구분 |
| 5 | `ad_kind_key` | `varchar` | 광고상품 key |
| 5 | `ad_kind_group` | `varchar` | 광고상품그룹 |
| 5 | `is_bmclub` | `tinyint` | 배민클럽여부 |
| 5 | `bmclub_benefit_amt` | `bigint` | 배민클럽혜택금액 |
| 5 | `is_flexible_dlvry_change` | `tinyint` | 탄력배달변경여부 (F/O - 2025-07-22) |
| 5 | `flexible_dlvry_tip` | `bigint` | 탄력배달팁  (F/O - 2025-07-22) |
| 5 | `shop_service_type` | `varchar` | 가게서비스유형 |
| 5 | `instdc_ord_discount_amt` | `bigint` | 즉시할인주문할인금액 |
| 5 | `instdc_dlvry_tip_discount_amt` | `bigint` | 즉시할인배달팁할인금액 |
| 5 | `bmclub_benefit_ord_amt` | `bigint` | 배민클럽혜택주문금액 |
| 5 | `bmclub_benefit_dlvry_tip` | `bigint` | 배민클럽혜택배달팁 |
| 5 | `org_dlvry_tip` | `bigint` | 원본배달팁 |
| 5 | `fee_pickad_policy_cd` | `varchar` | 수수료선택광고정책코드 |
| 5 | `fee_discount_pickad_policy_cd` | `varchar` | 수수료할인선택광고정책코드  (`,` 로 구분) |
| 5 | `fee_discount_rate` | `double` | 수수료할인비율 |
| 5 | `last_fee_rate` | `double` | 최종수수료비율 |
| 5 | `dlvry_cost_pickad_policy_cd` | `varchar` | 배달비선택광고정책코드 |
| 5 | `dlvry_cost_discount_pickad_policy_cd` | `varchar` | 배달비할인선택광고정책코드 (`,` 로 구분) |
| 5 | `dlvry_cost_discount_amt` | `bigint` | 배달비할인금액 |
| 5 | `last_dlvry_cost` | `bigint` | 최종배달비 |
| 5 | `is_mfo` | `tinyint` | MFO 여부 |
| 5 | `mfo_dlvry_tip_discount_amt` | `bigint` | MFO 배달팁할인금액 |
| 5 | `hva_dlvry_tip_discount_amt` | `bigint` | HVA 배달팁할인금액 |
| 5 | `free_dlvry_promo_dlvry_tip_discount_amt` | `bigint` | 무료배달프로모션배달팁할인금액 |
| 5 | `is_timesale` | `tinyint` | 타임세일  여부 |
| 5 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `ord_item_info`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `ord_item_id` | `varchar` | 주문아이템 ID |
| 2 | `svc_type` | `varchar` | 서비스유형 |
| 2 | `ord_no` | `varchar` | 주문번호 |
| 2 | `mem_no` | `varchar` | 회원번호 |
| 2 | `shop_no` | `varchar` | 가게번호 |
| 2 | `food_ord_status_cd` | `varchar` | 푸드주문상태코드 |
| 2 | `ord_dttm` | `timestamp(9)` | 주문일시 |
| 2 | `item_id` | `varchar` | 아이템 ID |
| 2 | `item_nm` | `varchar` | 아이템이름 |
| 2 | `item_ord_amt` | `bigint` | 아이템주문금액 |
| 2 | `item_price` | `integer` | 아이템가격 |
| 2 | `item_qty` | `bigint` | 아이템수량 |
| 2 | `menu_discount_amt` | `bigint` | 메뉴할인금액 |
| 2 | `franchise_promo_discount_amt` | `bigint` | 프랜차이즈프로모션할인금액 |
| 2 | `shop_promo_discount_amt` | `bigint` | 가게프로모션할인금액 |
| 2 | `franchise_charge_amt` | `bigint` | 프랜차이즈부담금액 |
| 2 | `seller_charge_amt` | `bigint` | 판매자부담금액 |
| 2 | `is_free_opt_incld` | `tinyint` | 무료옵션포함여부 |
| 2 | `is_paid_opt_incld` | `tinyint` | 유료옵션포함여부 |
| 2 | `menu_cate_nm` | `varchar` | 메뉴카테고리이름 |
| 2 | `is_rep_menu` | `tinyint` | 대표메뉴여부 |
| 2 | `is_popular_menu` | `tinyint` | 인기메뉴여부 |
| 2 | `is_alcohol` | `tinyint` | 주류여부 |
| 2 | `food_dlvry_type_cd` | `varchar` | 푸드배달유형코드 |
| 2 | `ord_rgn3_cd` | `varchar` | 주문지역소분류코드 |
| 2 | `shop_cate_cd` | `varchar` | 가게카테고리코드 |
| 2 | `franchise_no` | `varchar` | 프랜차이즈번호 |
| 2 | `gender_cd` | `varchar` | 성별코드 |
| 2 | `age` | `integer` | 연령 |
| 2 | `is_mem` | `tinyint` | 회원여부 |
| 2 | `is_cmplt_ord` | `tinyint` | 완료주문여부 |
| 2 | `is_test` | `tinyint` | 테스트여부 |
| 2 | `is_stod` | `tinyint` | 알뜰배달여부 |
| 2 | `is_bmclub` | `tinyint` | 배민클럽여부 |
| 2 | `ad_kind_cd` | `varchar` | 광고상품코드 |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `sbstore_hist`

### 📄 Table: `shop_master`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 5 | `shop_no` | `varchar` | 가게번호 |
| 5 | `shop_name` | `varchar` | 가게명 |
| 5 | `shop_owner_no` | `varchar` | 업주번호 |
| 5 | `shop_service_type` | `varchar` | 가게 서비스타입 |
| 5 | `shop_category` | `varchar` | 카테고리코드 |
| 5 | `shop_status` | `varchar` | 차단여부 |
| 5 | `franchise_no` | `varchar` | 프랜차이즈  번호 |
| 5 | `franchise_nm` | `varchar` | 프랜차이즈  이름 |
| 5 | `biz_no` | `varchar` | 사업자등록증  번호 |
| 5 | `telephone` | `varchar` | 가게 전화번호 |
| 5 | `virtual_telephone` | `varchar` | 가상 전화번호 |
| 5 | `is_ad` | `tinyint` | 광고 진행 여부( 리스팅  광고만 ) |
| 5 | `is_shop_test` | `tinyint` | 테스트  가게 여부 |
| 5 | `order_take_channel_type` | `varchar` | 가게 설정 접수채널 |
| 5 | `minimum_order_price` | `integer` | 최소주문금액 |
| 5 | `is_baropay` | `tinyint` | 바로결제  사용여부 |
| 5 | `zip_code` | `varchar` | 가게 우편번호 |
| 5 | `address` | `varchar` | 가게 주소 |
| 5 | `address_det` | `varchar` | 가게 상세주소 |
| 5 | `latitude` | `varchar` | 위도 |
| 5 | `longitude` | `varchar` | 경도 |
| 5 | `rgn1_cd` | `varchar` | 지역1 코드 ( 법정동  전환 기간 : 2018-07-01~) |
| 5 | `rgn2_cd` | `varchar` | 지역2 코드 ( 법정동  전환 기간 : 2018-07-01~) |
| 5 | `rgn3_cd` | `varchar` | 지역3 코드 ( 법정동  전환 기간 : 2018-07-01~) |
| 5 | `dsm_no` | `varchar` | dsm 번호 |
| 5 | `dsm_name` | `varchar` | DSM 이름 |
| 5 | `dsm_type` | `varchar` | DSM 타입코드 |
| 5 | `manager_no` | `varchar` | 매니저  번호 |
| 5 | `company_no` | `varchar` | 기업번호  ( 상호번호 ) |
| 5 | `company_name` | `varchar` | DSM 의 상위회사 |
| 5 | `head_office_company_no` | `varchar` | 최상위  회사 번호 |
| 5 | `company_type` | `varchar` | 기업 구분 코드 |
| 5 | `biz_scale` | `varchar` | 중소상공인  분류 |
| 5 | `pref_rate` | `double` | 우대 수수료율 |
| 5 | `is_reservation` | `tinyint` | 예약주문  가능여부 |
| 5 | `is_takeout` | `tinyint` | 테이크아웃  가능 여부 |
| 5 | `is_takeout_discount` | `tinyint` | 테이크아웃  할인 여부 |
| 5 | `is_minimum_order_amount_discount` | `tinyint` | 포장최소주문금액여부  (2025-07-22 F/O) |
| 5 | `takeout_discount_rate` | `integer` | 포장할인비율  (2025-07-22 F/O) |
| 5 | `takeout_discount_type` | `varchar` | 포장할인유형코드  (2025-07-22 F/O) |
| 5 | `takeout_discount_fee` | `integer` | 포장할인금액  (2025-07-22 F/O) |
| 5 | `created_at` | `timestamp(9)` | 등록시각 |
| 5 | `modified_at` | `timestamp(9)` | 수정시각 |
| 5 | `small_order_fee` | `integer` | 소액주문비  금액 |
| 5 | `is_baemin_one` | `tinyint` | 배민1 가게 여부 |
| 5 | `origin_shop_service_type` | `varchar` | 이전가게  서비스타입  - f/o(2025-09-23) |
| 5 | `origin_shop_no` | `varchar` | 가게 정보를  복사한  원본 가게 번호, 배민-> 배민1 복사 경우만  발생 - f/o(2025-09-23) |
| 5 | `minimum_order_price_detail_map` | `array(row(holiday tinyint, time_range varchar, minimum_order_price bigint)` | ) 최소주문금액  상세( 통합형 ) |
| 5 | `delivery_type` | `varchar` | 배달 유형 |
| 5 | `is_od` | `tinyint` | OD 여부 |
| 5 | `is_mp` | `tinyint` | MP 여부 |
| 5 | `is_visit` | `tinyint` | 방문여부 |
| 5 | `is_bmclub` | `tinyint` | 배민클럽  여부 |
| 5 | `exclsv_shop_grade_det_cd` | `varchar` | 단독가게등급상세코드 |
| 5 | `part_date` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `cl_food`

### 📄 Table: `franchise_grp_grade_info`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `franchise_no` | `varchar` | 프랜차이즈번호 |
| 4 | `franchise_nm` | `varchar` | 프랜차이즈이름 |
| 4 | `franchise_reg_dt` | `varchar` | 프랜차이즈등록일자 |
| 4 | `franchise_mod_dt` | `varchar` | 프랜차이즈수정일자 |
| 4 | `franchise_grp_nm` | `varchar` | 프랜차이즈그룹이름 |
| 4 | `rep_shop_cate_cd` | `varchar` | 대표가게카테고리코드 |
| 4 | `base_dt` | `varchar` | 기준일자 |
| 4 | `ord_amt_rank` | `bigint` | 주문금액순위 |
| 4 | `ord_amt_grade_cd` | `varchar` | 주문금액등급코드 |
| 4 | `franchise_grp_mod_dt` | `varchar` | 프랜차이즈그룹수정일자 |

## 📁 Schema: `sbcpn`

### 📄 Table: `contribution`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 5 | `contribution_id` | `varchar` | PK : contribution_id |
| 5 | `coupon_group_seq` | `varchar` | 쿠폰그룹  SEQ |
| 5 | `amount` | `bigint` | 분담금액 |
| 5 | `rate` | `double` | 분담금비율 |
| 5 | `cash_receipt_amount` | `bigint` | 현금영수증금액 |
| 5 | `owner` | `varchar` | 분담 주체 |
| 5 | `created_at` | `timestamp(9)` | - |
| 5 | `vendor_code` | `varchar` | 거래처코드 |
| 5 | `vendor_name` | `varchar` | 거래처이름 |

### 📄 Table: `cpn_grp`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `cpn_grp_seq` | `integer` | autoincrement 되는 primary key |
| 4 | `reg_id` | `varchar` | 등록자 |
| 4 | `reg_date` | `timestamp(9)` | 등록일시 |
| 4 | `mod_id` | `varchar` | 수정자 |
| 4 | `mod_date` | `timestamp(9)` | 수정일시 |
| 4 | `att_cont` | `varchar` | 유의사항 |
| 4 | `calc_ty_cd` | `varchar` | 정산구분코드  (B0383) |
| 4 | `cpn_code` | `varchar` | 쿠폰코드 |
| 4 | `cpn_code_ty_cd` | `varchar` | 쿠폰코드구분코드 (B0332) |
| 4 | `amount_ty_cd` | `varchar` | 수량유형코드 |
| 4 | `cpn_grp_id` | `varchar` | 쿠폰그룹 ID |
| 4 | `reg_ty_cd` | `varchar` | 발급유형코드 |
| 4 | `cpn_grp_st_cd` | `varchar` | 쿠폰그룹상태코드 |
| 4 | `use_date_ty_cd` | `varchar` | 결제기간설정타입코드 |
| 4 | `cpn_mng_nm` | `varchar` | 쿠폰그룹이름 |
| 4 | `cpn_nm` | `varchar` | 쿠폰노출명 |
| 4 | `cpn_pub_cd` | `varchar` | 쿠폰발급코드 |
| 4 | `deduct_amt` | `integer` | 공재금액 |
| 4 | `discount_price` | `integer` | 할인금액 |
| 4 | `discount_rt` | `integer` | 할인율 |
| 4 | `dup_use_able_yn` | `varchar` | 중복가능사용여부 |
| 4 | `first_purch_chk_yn` | `varchar` | 첫바로결제  여부 |
| 4 | `issue_limit_qty` | `integer` | 발급제한수량 |
| 4 | `issue_rmn_qty` | `integer` | 발급잔여수량 |
| 4 | `max_discount_price` | `integer` | 최대할인금액 |
| 4 | `min_ord_price` | `integer` | 최소주문금액 |
| 4 | `reg_able_date_b` | `timestamp(9)` | 발급가능시작일자 |
| 4 | `reg_able_date_e` | `timestamp(9)` | - |
| 4 | `reg_stop_msg` | `varchar` | 발급 임시 중단 상태의  메세지 |
| 4 | `remark` | `varchar` | 비고 |
| 4 | `repeat_reg_able_yn` | `varchar` | 반복발급가능여부 |
| 4 | `repeat_reg_cnt` | `smallint` | 반복발급수량 |
| 4 | `repeat_use_able_yn` | `varchar` | 반복사용가능여부 |
| 4 | `use_able_date_b` | `timestamp(9)` | 사용가능시작일자 |
| 4 | `use_able_date_e` | `timestamp(9)` | 사용가능종료일자 |
| 4 | `use_able_term_cfg_yn` | `varchar` | 사용가능기간시간설정여부 |
| 4 | `use_able_term_time` | `smallint` | 사용가능기간시간 |
| 4 | `use_limit_qty` | `integer` | 사용제한수량 |
| 4 | `use_stop_msg` | `varchar` | 사용 임시 중단 상태의  메세지 |
| 4 | `cpn_camp_seq` | `integer` | 쿠폰 캠페인  seq |
| 4 | `user_seq` | `smallint` | 사용자번호 |
| 4 | `reg_dt` | `varchar` | 등록일 |
| 4 | `first_payment_chk_yn` | `varchar` | 첫 결제 여부 |
| 4 | `cpn_grp_ver` | `varchar` | 쿠폰 그룹 버전 |
| 4 | `cash_amount` | `bigint` | 현금영수증  금액 |
| 4 | `pricing_type` | `varchar` | 금액 타입(PAID : 유상,FREE : 무상) |
| 4 | `pricing_desc` | `varchar` | 금액 비고 |
| 4 | `service_code` | `varchar` | 서비스코드 (BAEMIN : 배달의민족 ,MARKET : B 마트,BAEMIN_STORE : 배민스토어 ) |
| 4 | `discount_target` | `varchar` | 할인대상 |
| 4 | `use_able_delay_days` | `integer` | 발급 후 지연일수  (0 이면 발급일  포함, 1 이상이면  X 일 후부터 ) |

### 📄 Table: `cpn_camp`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `cpn_camp_seq` | `integer` | autoincrement 되는 primary key |
| 4 | `reg_id` | `varchar` | 등록자 |
| 4 | `reg_date` | `timestamp(9)` | 등록일자 |
| 4 | `mod_id` | `varchar` | 수정자 |
| 4 | `mod_date` | `timestamp(9)` | 수정일자 |
| 4 | `appr_doc_no` | `varchar` | 결재문서번호 |
| 4 | `camp_id` | `varchar` | 캠페인 ID |
| 4 | `camp_nm` | `varchar` | 캠페인이름 |
| 4 | `camp_purpose_cd` | `varchar` | 캠페인목적코드 |
| 4 | `remark` | `varchar` | 비고 |
| 4 | `user_seq` | `smallint` | - |
| 4 | `del_yn` | `varchar` | - |
| 4 | `reg_dt` | `varchar` | 등록일 |

## 📁 Schema: `coupon_mart`

### 📄 Table: `coupon_master`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 5 | `service_type` | `varchar` | 서비스  유형 |
| 5 | `delivery_type` | `varchar` | 배달 유형 |
| 5 | `mem_no` | `varchar` | 회원번호 |
| 5 | `dvc_id` | `varchar` | 기기번호 |
| 5 | `coupon_id` | `varchar` | 쿠폰( 그룹) 번호 |
| 5 | `coupon_name_display` | `varchar` | 노출 쿠폰( 그룹) 명 |
| 5 | `coupon_name_manage` | `varchar` | 관리 쿠폰( 그룹) 명 |
| 5 | `coupon_start_dttm` | `timestamp(9)` | 쿠폰( 그룹) 사용가능  시작일 |
| 5 | `coupon_end_dttm` | `timestamp(9)` | 쿠폰( 그룹) 사용 가능 만료일 |
| 5 | `member_coupon_id` | `varchar` | 회원별  쿠폰 번호 |
| 5 | `coupon_publish_system` | `varchar` | 쿠폰 발행 시스템  구분 |
| 5 | `coupon_discount_target` | `varchar` | 쿠폰 할인 적용 대상 |
| 5 | `coupon_issue_type` | `varchar` | 쿠폰 발급 유형 |
| 5 | `coupon_limit_use` | `map(varchar, array(varchar)` | ) 쿠폰 사용 조건 |
| 5 | `is_coupon_first_order` | `tinyint` | 서비스별  회원) 별 첫 주문 쿠폰 여부 |
| 5 | `is_coupon_shop` | `tinyint` | 배민/ 배라 특정가게  전용 쿠폰 여부 |
| 5 | `is_coupon_franchise` | `tinyint` | 프랜차이즈  전용 쿠폰 여부 |
| 5 | `is_coupon_baemin1` | `tinyint` | 배민1 여부 |
| 5 | `is_coupon_baemin` | `tinyint` | 배민 서비스  제한 조건 존재 |
| 5 | `is_coupon_baera` | `tinyint` | 배라 서비스  제한 조건 존재 |
| 5 | `is_coupon_baeminpay` | `tinyint` | 배민페이  전용 쿠폰 여부 |
| 5 | `discount_rate` | `real` | 할인율 |
| 5 | `maximum_discount_amount` | `bigint` | 최대 할인금액 |
| 5 | `minimum_order_amount` | `bigint` | 최소 주문금액 |
| 5 | `coupon_status` | `varchar` | 쿠폰 상태 |
| 5 | `coupon_issue_dttm` | `timestamp(9)` | 쿠폰 발급 일시 |
| 5 | `coupon_use_dttm` | `timestamp(9)` | 쿠폰사용일시 |
| 5 | `company_charge_rate` | `real` | 자사 분담율 |
| 5 | `seller_charge_rate` | `real` | 판매자  분담율 |
| 5 | `company_charge_amount` | `bigint` | 자사 분담금 |
| 5 | `seller_charge_amount` | `bigint` | 판매자  분담금 |
| 5 | `ord_no` | `varchar` | 주문번호 |
| 5 | `order_status` | `varchar` | 주문상태 |
| 5 | `order_amount` | `bigint` | 주문금액 |
| 5 | `total_delivery_amount` | `bigint` | 고객이  지불한  배송/ 배달금액  총액 |
| 5 | `coupon_discount_amount` | `bigint` | 쿠폰 할인액 |
| 5 | `is_first_order` | `tinyint` | 서비스  첫주문여부 |
| 5 | `is_test` | `tinyint` | 테스트  주문 여부 |
| 5 | `is_order_closed` | `tinyint` | 완료 주문 여부 |
| 5 | `shop_no` | `varchar` | 가게번호 |
| 5 | `center_no` | `varchar` | 지점번호 |
| 5 | `seller_no` | `varchar` | 셀러번호 |
| 5 | `broadcast_id` | `varchar` | 방송ID |
| 5 | `customer_rgn3_cd` | `varchar` | 고객지역코드 3 ( 법정동  전환 기간 : 2018-05-01~) |
| 5 | `is_pluscpn` | `tinyint` | 더하기쿠폰여부 |
| 5 | `is_bmclub_cpn` | `tinyint` | 배민클럽쿠폰여부 |
| 5 | `part_date` | `varchar` | **[파티션 키]**  |
| 5 | `part_svc` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `menucommon`

### 📄 Table: `promotion`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `promotion_id` | `varchar` | ID |
| 4 | `type` | `varchar` | 기본할인 / 묶음할인 / 조건할인 / 서비스제공 |
| 4 | `discount_type` | `varchar` | 정액/ 정률/ 서비스 ( 무료) - 프로모션  유형 (cf. 한정기간 , 한정시간의  경우 타입으로  관리하지  않고 start_date,time | end_date,time 으로 판단) |
| 4 | `discount_value` | `integer` | 할인값 ( 정률의  경우 소수점  오차가  없이 계산되어야  하기 때문에  부동소수점  float 가 아닌 고정소수점  decimal 사용) |
| 4 | `status` | `varchar` | 프로모션  상태 ( 대기, 진행, 종료/ 강제종료 ) - 대기, 진행, 종료 여부는  NORMAL 상태에서  start_date, end_date 를 보고 판단한다 |
| 4 | `franchise_yn` | `tinyint` | 프랜차이즈  여부 |
| 4 | `start_date` | `timestamp(9)` | 프로모션  시작일시 |
| 4 | `end_date` | `timestamp(9)` | 프로모션  종료일시 |
| 4 | `stopped_at` | `timestamp(9)` | 강제 종료 일자 |
| 4 | `channel_type` | `varchar` | 채널타입 |
| 4 | `created_at` | `timestamp(9)` | 생성일 |
| 4 | `modified_at` | `timestamp(9)` | 수정일 |
| 4 | `target_type` | `varchar` | 프로모션  타입( 메뉴/ 옵션) |

### 📄 Table: `promotion_franchise`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `promotion_id` | `varchar` | 프로모션 ID |
| 4 | `franchise_id` | `varchar` | 프랜차이즈 ID |
| 4 | `franchise_budam_price` | `double` | 본사부담가격 |
| 4 | `except_shop_ids` | `varchar` | 프로모션  제외 가게 아이디  목록 |
| 4 | `shop_owner_budam_price` | `double` | 업주부담가격 |

## 📁 Schema: `vl_food`

### 📄 Table: `vfd_b2c_fact_daily`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 3 | `ord_no` | `varchar` | - |
| 3 | `coupon_discount_total` | `bigint` | - |
| 3 | `coupon_discount_b2c` | `bigint` | - |
| 3 | `coupon_discount_all` | `bigint` | - |
| 3 | `coupon_discount_first` | `bigint` | - |
| 3 | `coupon_discount_re` | `bigint` | - |
| 3 | `coupon_discount_b2b` | `bigint` | - |
| 3 | `coupon_discount_3p` | `bigint` | - |
| 3 | `pickup_discount` | `bigint` | - |
| 3 | `menu_discount` | `bigint` | - |
| 3 | `menu_discount_b2c` | `bigint` | - |
| 3 | `menu_discount_b2c_mfo_day` | `bigint` | - |
| 3 | `menu_discount_b2c_mfo_time` | `bigint` | - |
| 3 | `menu_discount_b2c_normal_day` | `bigint` | - |
| 3 | `menu_discount_b2c_normal_time` | `bigint` | - |
| 3 | `menu_discount_b2b` | `double` | - |
| 3 | `menu_discount_b2b_mfo_day` | `double` | - |
| 3 | `menu_discount_b2b_mfo_time` | `double` | - |
| 3 | `menu_discount_b2b_normal_day` | `double` | - |
| 3 | `menu_discount_b2b_normal_time` | `double` | - |
| 3 | `deliverytip_discount` | `bigint` | - |
| 3 | `deliverytip_discount_order` | `bigint` | - |
| 3 | `deliverytip_discount_deliverytip` | `bigint` | - |
| 3 | `instant_discount` | `bigint` | - |
| 3 | `instant_discount_order` | `bigint` | - |
| 3 | `instant_discount_deliverytip` | `bigint` | - |
| 3 | `instant_discount_all_order` | `bigint` | - |
| 3 | `instant_discount_first_order` | `bigint` | - |
| 3 | `instant_discount_re_order` | `bigint` | - |
| 3 | `instant_discount_bmclub_order` | `bigint` | - |
| 3 | `instant_discount_bmclub_deliverytip` | `bigint` | - |
| 3 | `instant_discount_free_deliverytip` | `bigint` | - |
| 3 | `instant_discount_amount_deliverytip` | `bigint` | - |
| 3 | `instant_discount_woowa` | `bigint` | - |
| 3 | `instant_discount_order_woowa` | `bigint` | - |
| 3 | `instant_discount_deliverytip_woowa` | `bigint` | - |
| 3 | `instant_discount_all_order_woowa` | `bigint` | - |
| 3 | `instant_discount_first_order_woowa` | `bigint` | - |
| 3 | `instant_discount_re_order_woowa` | `bigint` | - |
| 3 | `instant_discount_bmclub_order_woowa` | `bigint` | - |
| 3 | `instant_discount_bmclub_deliverytip_woowa` | `bigint` | - |
| 3 | `instant_discount_free_deliverytip_woowa` | `bigint` | - |
| 3 | `instant_discount_amount_deliverytip_woowa` | `bigint` | - |
| 3 | `is_bmclub_order` | `integer` | - |
| 3 | `bmclub_benefit_amt` | `integer` | - |
| 3 | `coupon_discount_woowa` | `double` | - |
| 3 | `coupon_discount_b2b_woowa` | `double` | - |
| 3 | `coupon_discount_3p_woowa` | `double` | - |
| 3 | `menu_discount_b2b_woowa` | `double` | - |
| 3 | `menu_discount_b2b_owner` | `double` | - |
| 3 | `menu_discount_b2b_mfo_day_owner` | `double` | - |
| 3 | `menu_discount_b2b_mfo_time_owner` | `double` | - |
| 3 | `menu_discount_b2b_normal_day_owner` | `double` | - |
| 3 | `menu_discount_b2b_normal_time_owner` | `double` | - |
| 3 | `instant_discount_all_order_promotion` | `bigint` | - |
| 3 | `instant_discount_first_order_promotion` | `bigint` | - |
| 3 | `instant_discount_re_order_promotion` | `bigint` | - |
| 3 | `instant_discount_bmclub_order_promotion` | `bigint` | - |
| 3 | `instant_discount_free_deliverytip_promotion` | `bigint` | - |
| 3 | `instant_discount_amount_deliverytip_promotion` | `bigint` | - |
| 3 | `instant_discount_all_order_promotion_woowa` | `bigint` | - |
| 3 | `instant_discount_first_order_promotion_woowa` | `bigint` | - |
| 3 | `instant_discount_re_order_promotion_woowa` | `bigint` | - |
| 3 | `instant_discount_bmclub_order_promotion_woowa` | `bigint` | - |
| 3 | `instant_discount_free_deliverytip_promotion_woowa` | `bigint` | - |
| 3 | `instant_discount_amount_deliverytip_promotion_woowa` | `bigint` | - |
| 3 | `timesale_order` | `bigint` | - |
| 3 | `b2b_timesale_order` | `bigint` | - |
| 3 | `b2c_timesale_order` | `bigint` | - |
| 3 | `timesale_order_woowa` | `bigint` | - |
| 3 | `b2b_timesale_order_woowa` | `bigint` | - |
| 3 | `b2c_timesale_order_woowa` | `bigint` | - |
| 3 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `vfd_b2c_mp_free_deliverytip_fact_daily`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 3 | `ord_no` | `varchar` | - |
| 3 | `mp_free_delivery_total` | `integer` | - |
| 3 | `mp_free_delivery_whole` | `integer` | - |
| 3 | `mp_free_delivery_base` | `integer` | - |
| 3 | `deliverytip_discount` | `double` | - |
| 3 | `part_date` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `delivery_mart`

### 📄 Table: `delivery_master`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `ord_no` | `varchar` | 주문번호 . beamin_store 경우 order_sheet_no 를 의미 |
| 4 | `split_ord_no` | `varchar` | 비마트  분리주문번호 |
| 4 | `service_type` | `varchar` | 서비스유형  (BAEMIN | BAERA | BMART) |
| 4 | `delivery_no` | `varchar` | 배달번호 |
| 4 | `rider_no` | `varchar` | 라이더 ID. OD 의 경우 원본 id 그대로  사용. VD( 배달대행 ) 의 경우 {agency_id}_{ 비식별화된 )rider_key 구조} |
| 4 | `shop_no` | `varchar` | 가게번호 . bmart 경우 baemin_shop_no, beamin_store 경우 branch_id 를 의미 |
| 4 | `mem_no` | `varchar` | 회원번호 |
| 4 | `order_status` | `varchar` | 주문 상태 (CLOSED | CANCELLED | FAILED | DENIED | ACCEPTED) |
| 4 | `shop_category` | `varchar` | 가게 카테고리 |
| 4 | `shop_rgn3_cd` | `varchar` | 가게 지역구분코드 3 ( 법정동  전환 기간 : 2019-06-17~) |
| 4 | `customer_rgn3_cd` | `varchar` | 배달지  지역구분코드 3 ( 법정동  전환 기간 : 2019-06-17~) |
| 4 | `distance` | `integer` | 가게 ~ 배달지  거리(m) |
| 4 | `delivery_type` | `varchar` | 배달유형  [OD: Own delivery(Bros), VD-Agency: 배달대행사  연동된  주문건 , VD-Self: 따로 연동되지  않아 배달정보를  알 수 없는 주문건 ] |
| 4 | `interface_type` | `varchar` | 배달대행사  interface 방식. DLL | API | FOODTECH |
| 4 | `agency` | `varchar` | 배달대행사  이름. VD( 배달대행 ) 배달건만  존재 |
| 4 | `delivery_status` | `varchar` | 배달상태  (RECEIPT | RIDER_ASSIGNED | COMPLETED_DELIVERY | CANCEL_DELIVERY | UNDEFINED) |
| 4 | `delivery_method` | `varchar` | 배달수단 . OD(Bros 를 통한 배달) 만 존재 |
| 4 | `delivery_order` | `integer` | 배달순서 . 1 부터 시작하여  순차적으로  증가함 . 2 이상인  값은 OD(Bros 를 통한 배달) 만 데이터  존재 |
| 4 | `additional_delivery_reason_type` | `varchar` | 추가 배달 사유. OD(Bros 를 통한 배달) 만 존재 |
| 4 | `ad_campaign_id` | `varchar` | 광고인벤토리  ID |
| 4 | `ad_inventory_key` | `varchar` | 인벤토리  Key |
| 4 | `rider_type` | `varchar` | 라이더유형 . OD(Bros 를 통한 배달) 만 존재 |
| 4 | `center_id` | `varchar` | 라이더센터 ID. OD(Bros 를 통한 배달) 만 존재 |
| 4 | `center_name` | `varchar` | 라이더센터명 . OD(Bros 를 통한 배달) 만 존재 |
| 4 | `order_date` | `timestamp(9)` | 주문시각 |
| 4 | `delivery_accept_date` | `timestamp(9)` | 배달접수시각 |
| 4 | `allocated_date` | `timestamp(9)` | 배차완료시각 |
| 4 | `pickup_date` | `timestamp(9)` | 라이더픽업시각 |
| 4 | `hand_over_date` | `timestamp(9)` | 배달완료시각 |
| 4 | `delivery_expected_minutes` | `array(integer)` | 배달예상시간 . delivery_expected_minutes[0]: 예상시간  min. delivery_expected_minutes[1]: 예상시간  max |
| 4 | `customer_notified_minute` | `integer` | 고객에게  안내된  배달시간 ( 예: 40 분) |
| 4 | `delivery_time_minute` | `real` | 총 배달소요시간 ( 분)( 배달접수  ~ 배달완료 ) |
| 4 | `is_punctual` | `integer` | 고객에게  안내한  배달시각  준수여부 . (1 | 0) |
| 4 | `bros_times` | `map(varchar, timestamp(9)` | ) bros 관련 시각 COOK_REQUEST_DATE: 조리요청시각 , PICKUP_GUIDE_DATE: 픽업기준시각 , RIDER_NOTIFICATION_DATE: AI 모드 시 라이더향  배달목표시각 , TARGETED_RIDER_DELIVERY_DATE_TIME: 일반배차  라이더향  배달목표시각 |
| 4 | `bmart_times` | `map(varchar, timestamp(9)` | ) bmart 시각 map. bmart_times['PICKING_DATE']: picking 시각, bmart_times['PACKING_DATE']: packing 시각, bmart_times['WAITING_RELEASE_DATE']: 출고대기  시각 |
| 4 | `cook_minute` | `integer` | 조리시간 |
| 4 | `ord_price` | `bigint` | 주문금액 |
| 4 | `extra_delivery_tip` | `bigint` | 거리 초과 할증 배달팁 |
| 4 | `delivery_tip` | `bigint` | 고객이  내는 배달팁 |
| 4 | `rider_delivery_fee` | `bigint` | 라이더에게  지급하는  배달료 |
| 4 | `is_test` | `integer` | 테스트  데이터  여부 (1 | 0) |
| 4 | `is_closed` | `integer` | 배달 정상 종료 여부 (1 | 0) |
| 4 | `is_single_delivery` | `integer` | 단건배달여부 . OD(Bros 를 통한 배달) 만 존재 |
| 4 | `is_fast_free_delivery` | `integer` | 번쩍배달여부 . OD(Bros 를 통한 배달) 만 존재 |
| 4 | `is_auto_allocated` | `integer` | ai 배차 여부 (1 | 0) |
| 4 | `is_meet_payment` | `integer` | 만나서  결제 여부. (1 | 0) |
| 4 | `bros_business_day` | `varchar` | bros 영업일 . 사용 시 part_date 를 bors 영업 시작일  ~ bros 영업 종료일  다음날까지  제한하여  함께 사용해야  함. ex)WHERE bros_busines_day = '2021-05-05' AND part_date >= '2021-05-05' AND part_date < '2021-05-07' |
| 4 | `is_stod` | `tinyint` | 알뜰배달  주문 여부. 배민1(BAERA) 일반( 묶음) 배달 서비스를  제공하는  상품 주문의  구분 |
| 4 | `is_flexible_dlvry_change` | `tinyint` | 탄력배달  변경 여부 |
| 4 | `part_date` | `varchar` | **[파티션 키]**  |
| 4 | `part_svc` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `sbsvc`

### 📄 Table: `ord_item`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `ord_no` | `varchar` | 주문번호 |
| 4 | `shop_no` | `varchar` | 업소번호 |
| 4 | `order_status` | `varchar` | 주문상태 |
| 4 | `service_type` | `varchar` | 서비스타입 |
| 4 | `purchase_type` | `varchar` | 결제타입 |
| 4 | `reason_code` | `varchar` | 사유코드 |
| 4 | `item_description` | `varchar` | 메뉴 상세 설명 |
| 4 | `item_mapping_id` | `varchar` | 메뉴 아이디 |
| 4 | `item_name` | `varchar` | 메뉴명 |
| 4 | `item_price` | `bigint` | 메뉴가격 |
| 4 | `item_quantity` | `integer` | 메뉴수량 |
| 4 | `part_date` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `sbbi`

### 📄 Table: `dim_date_cd`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 3 | `date_cd` | `varchar` | 기준일자 |
| 3 | `week_cd` | `varchar` | 주코드 |
| 3 | `month_cd` | `varchar` | 월코드 |
| 3 | `weekstart_dt` | `date` | 주시작일자 |
| 3 | `weekend_dt` | `date` | 주종료일자 |
| 3 | `monthstart_dt` | `date` | 월시작일자 |
| 3 | `monthend_dt` | `date` | 월종료일자 |
| 3 | `year_nm` | `varchar` | 년도 |
| 3 | `month_nm` | `varchar` | 월 |
| 3 | `day_nm` | `varchar` | 일 |
| 3 | `week_nm` | `varchar` | 요일이름 |
| 3 | `holiday_yn` | `varchar` | 휴일 여부 |
| 3 | `holiday_desc` | `varchar` | 휴일 설명 |
| 3 | `use_yn` | `varchar` | 사용 여부 |
| 3 | `std_dt` | `date` | 갱신일자 |
| 3 | `end_dt` | `date` | 종료일자 |
| 3 | `update_dt` | `timestamp(9)` | 갱신 타임스탬프 |
| 3 | `weekend_yn` | `varchar` | 주말 여부 |
| 3 | `public_holiday_yn` | `varchar` | 공휴일  여부 |
| 3 | `national_day_yn` | `varchar` | 국경일  여부 |
| 3 | `twentyfourdiv_day_yn` | `varchar` | 24 절기 여부 |
| 3 | `sundry_day_yn` | `varchar` | 잡절 여부 |
| 3 | `anniversary_day_yn` | `varchar` | 기념일  여부 |
| 3 | `public_holiday_desc` | `varchar` | 공휴일  설명 |
| 3 | `national_day_desc` | `varchar` | 국경일  설명 |
| 3 | `twentyfourdiv_day_desc` | `varchar` | 24 절기 설명 |
| 3 | `sundry_day_desc` | `varchar` | 잡절 설명 |
| 3 | `anniversary_day_desc` | `varchar` | 기념일  설명 |
| 3 | `days_desc` | `varchar` | 특일 설명( 공휴일 , 국경일 , 24 절기, 잡절, 기념일  종합) |

### 📄 Table: `dim_Rgn_cd`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 3 | `rgn1_cd` | `varchar` | 지역대분류코드 |
| 3 | `rgn2_cd` | `varchar` | 지역중분류코드 |
| 3 | `rgn3_cd` | `varchar` | 지역소분류코드 |
| 3 | `rgn1_nm` | `varchar` | 지역대분류명 |
| 3 | `rgn2_nm` | `varchar` | 지역중분류명 |
| 3 | `rgn3_nm` | `varchar` | 지역소분류명 |
| 3 | `rgn1_nm_eng` | `varchar` | 지역대분류영문명 |
| 3 | `rgn2_nm_eng` | `varchar` | 지역중분류영문명 |
| 3 | `rgn3_nm_eng` | `varchar` | 지역소분류영문명 |
| 3 | `short_rgn1_nm` | `varchar` | 짧은지역명 |
| 3 | `use_yn` | `varchar` | 사용여부 |
| 3 | `registered` | `varchar` | - |
| 3 | `modified` | `varchar` | - |
| 3 | `update_dt` | `timestamp(9)` | 업데이트일 |

### 📄 Table: `dim_cate_cd`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `category` | `varchar` | - |
| 1 | `display_name` | `varchar` | - |
| 1 | `english_name` | `varchar` | 카테고리영문명  - 2024-12-09 운영 F/O |
| 1 | `service_type` | `varchar` | - |
| 1 | `type` | `varchar` | - |
| 1 | `old_cate_cd` | `varchar` | 구 카테고리  코드 - 2024-12-09 운영 F/O |
| 1 | `sort_sequence` | `integer` | 정렬 시퀀스  - 2024-12-09 운영 F/O |
| 1 | `old_cate_nm` | `varchar` | 구 카테고리  이름 - 2024-12-09 운영 F/O |
| 1 | `use_yn` | `varchar` | - |
| 1 | `new_category` | `varchar` | - |

## 📁 Schema: `gsheet`

### 📄 Table: `shc_data`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 4 | `ta_ym` | `bigint` | 연월 |
| 4 | `mct_brn` | `bigint` | 사업자번호 |
| 4 | `mct_nm` | `varchar` | 가게명 |
| 4 | `mct_ry_nm` | `varchar` | 카테고리 ( 신한카드  기준) |
| 4 | `gds_wid_trl_nm` | `varchar` | RGN1 |
| 4 | `gds_dsr_nm` | `varchar` | RGN2 |
| 4 | `vlg_nm` | `varchar` | RGN3 |
| 4 | `gds_af_mct_ar` | `varchar` | 주소 |
| 4 | `lal_mct_xc_vl` | `double` | 경도 |
| 4 | `lal_mct_yc_vl` | `double` | 위도 |
| 4 | `rank_1_amt` | `double` | 금액순백분율 _ 전체( 광역시도 ) |
| 4 | `rank_2_amt` | `double` | 금액순백분율 _ 전체( 시군구 ) |
| 4 | `rank_3_amt` | `double` | 금액순백분율 _ 전체( 읍면동 ) |
| 4 | `rank_1_cnt` | `double` | 건수순백분율 _ 전체( 광역시도 ) |
| 4 | `rank_2_cnt` | `double` | 건수순백분율 _ 전체( 시군구 ) |
| 4 | `rank_3_cnt` | `double` | 건수순백분율 _ 전체( 읍면동 ) |
| 4 | `rank_1_amt_off` | `double` | 금액순백분율 _ 오프라인 ( 광역시도 ) |
| 4 | `rank_2_amt_off` | `double` | 금액순백분율 _ 오프라인 ( 시군구 ) |
| 4 | `rank_3_amt_off` | `double` | 금액순백분율 _ 오프라인 ( 읍면동 ) |
| 4 | `rank_1_cnt_off` | `double` | 건수순백분율 _ 오프라인 ( 광역시도 ) |
| 4 | `rank_2_cnt_off` | `double` | 건수순백분율 _ 오프라인 ( 시군구 ) |
| 4 | `rank_3_cnt_off` | `double` | 건수순백분율 _ 오프라인 ( 읍면동 ) |
| 4 | `rank_1_amt_dlv` | `double` | 금액순백분율 _ 온라인 ( 광역시도 ) |
| 4 | `rank_2_amt_dlv` | `double` | 금액순백분율 _ 온라인 ( 시군구 ) |
| 4 | `rank_3_amt_dlv` | `double` | 금액순백분율 _ 온라인 ( 읍면동 ) |
| 4 | `rank_1_cnt_dlv` | `double` | 건수순백분율 _ 온라인 ( 광역시도 ) |
| 4 | `rank_2_cnt_dlv` | `double` | 건수순백분율 _ 온라인 ( 시군구 ) |
| 4 | `rank_3_cnt_dlv` | `double` | 건수순백분율 _ 온라인 ( 읍면동 ) |
| 4 | `bm_rt` | `double` | 오더구성비 _ 배달의민족 |
| 4 | `ygy_rt` | `double` | 오더구성비 _ 요기요 |
| 4 | `eats_rt` | `double` | 오더구성비 _ 쿠팡이츠 |
| 4 | `avg_tot` | `integer` | 평균금액 _ 전체 |
| 4 | `avg_dlv` | `integer` | 평균금액 _ 온라인 |
| 4 | `avg_off` | `integer` | 평균금액 _ 오프라인 |
| 4 | `dlv_hga_rt` | `double` | 배달비중 ( 금액) |
| 4 | `dlv_cnt_rt` | `double` | 배달비중 ( 건수) |
| 4 | `new_ctr_f` | `integer` | 신규 가맹점  구분 |
| 4 | `new_sls_f` | `integer` | 신규 가맹점  구분_ 매출 발생 기준 |
| 4 | `bm_ry_nm` | `varchar` | 세부 업종 구분_ 배민 |
| 4 | `sl_cz_nm` | `varchar` | 세부 업종 구분 |
| 4 | `dlv_2030_cnt_rt` | `double` | 2030 연령대  온라인  주문건수  비중 |
| 4 | `off_2030_cnt_rt` | `double` | 2030 연령대  오프라인  주문건수  비중 |
| 4 | `tot_2030_cnt_rt` | `double` | 2030 연령대  전체 주문건수  비중 |
| 4 | `dlv_4050_cnt_rt` | `double` | 4050 연령대  온라인  주문건수  비중 |
| 4 | `off_4050_cnt_rt` | `double` | 4050 연령대  오프라인  주문건수  비중 |
| 4 | `tot_4050_cnt_rt` | `double` | 4050 연령대  전체 주문건수  비중 |
| 4 | `dlv_10_cnt_rt` | `double` | 10 대 오더 건수 비중_ 온라인 |
| 4 | `off_10_cnt_rt` | `double` | 10 대 오더 건수 비중_ 오프라인 |
| 4 | `tot_10_cnt_rt` | `double` | 10 대 오더 건수 비중_ 전체 |
| 4 | `dlv_20_cnt_rt` | `double` | 10 대 오더 건수 비중_ 온라인 |
| 4 | `off_20_cnt_rt` | `double` | 10 대 오더 건수 비중_ 오프라인 |
| 4 | `tot_20_cnt_rt` | `double` | 10 대 오더 건수 비중_ 전체 |
| 4 | `dlv_30_cnt_rt` | `double` | 10 대 오더 건수 비중_ 온라인 |
| 4 | `off_30_cnt_rt` | `double` | 10 대 오더 건수 비중_ 오프라인 |
| 4 | `tot_30_cnt_rt` | `double` | 10 대 오더 건수 비중_ 전체 |
| 4 | `dlv_40_cnt_rt` | `double` | 10 대 오더 건수 비중_ 온라인 |
| 4 | `off_40_cnt_rt` | `double` | 10 대 오더 건수 비중_ 오프라인 |
| 4 | `tot_40_cnt_rt` | `double` | 10 대 오더 건수 비중_ 전체 |
| 4 | `dlv_50_cnt_rt` | `double` | 10 대 오더 건수 비중_ 온라인 |
| 4 | `off_50_cnt_rt` | `double` | 10 대 오더 건수 비중_ 오프라인 |
| 4 | `tot_50_cnt_rt` | `double` | 10 대 오더 건수 비중_ 전체 |
| 4 | `dlv_60_cnt_rt` | `double` | 10 대 오더 건수 비중_ 온라인 |
| 4 | `off_60_cnt_rt` | `double` | 10 대 오더 건수 비중_ 오프라인 |
| 4 | `tot_60_cnt_rt` | `double` | 10 대 오더 건수 비중_ 전체 |
| 4 | `dlv_m_cnt_rt` | `double` | 성별 오더 건수 비중_ 남성 |
| 4 | `off_m_cnt_rt` | `double` | 성별 오더 건수 비중_ 남성_ 오프라인 |
| 4 | `tot_m_cnt_rt` | `double` | 성별 오더 건수 비중_ 남성_ 전체 |
| 4 | `dlv_f_cnt_rt` | `double` | 성별 오더 건수 비중_ 여성 |
| 4 | `off_f_cnt_rt` | `double` | 성별 오더 건수 비중_ 여성_ 오프라인 |
| 4 | `tot_f_cnt_rt` | `double` | 성별 오더 건수 비중_ 여성_ 전체 |
| 4 | `bm_1mu_rt` | `double` | 배민_1 만원이하결제건비중 |
| 4 | `yg_1mu_rt` | `double` | 요기요 _1 만원이하결제건비중 |
| 4 | `cp_1mu_rt` | `double` | 쿠팡이츠 _1 만원이하결제건비중 |
| 4 | `tot_12d_cnt_rt` | `double` | 전체 1.2 만원이하결제건비중 |
| 4 | `tot_12u_cnt_rt` | `double` | 전체 1.2 만원초과결제건비중 |
| 4 | `dlv_12d_cnt_rt` | `double` | 온라인 ( 배달) 1.2 만원이하결제건비중 |
| 4 | `dlv_12u_cnt_rt` | `double` | 온라인 ( 배달) 1.2 만원초과결제건비중 |
| 4 | `off_12d_cnt_rt` | `double` | 오프라인  1.2 만원이하결제건비중 |
| 4 | `off_12u_cnt_rt` | `double` | 오프라인  1.2 만원초과결제건비중 |
| 4 | `off_5d_cnt_rt` | `double` | 오프라인  0.5 만원이하결제건비중 |
| 4 | `off_8d_cnt_rt` | `double` | 오프라인  0.8 만원이하결제건비중 |
| 4 | `tm_07_10_cnt_rt` | `double` | 07 시~10 시 전체 결제건수  비중 |
| 4 | `tm_11_13_cnt_rt` | `double` | 11 시~13 시 전체 결제건수  비중 |
| 4 | `tm_14_16_cnt_rt` | `double` | 14 시~16 시 전체 결제건수  비중 |
| 4 | `tm_17_20_cnt_rt` | `double` | 17 시~20 시 전체 결제건수  비중 |
| 4 | `tm_21_06_cnt_rt` | `double` | 21 시~06 시 전체 결제건수  비중 |
| 4 | `est_amt_tot` | `bigint` | 매출추정액 _ 전체 |
| 4 | `est_amt_off` | `bigint` | 매출추정액 _ 오프라인 |
| 4 | `est_amt_dlv` | `bigint` | 매출추정액 _ 온라인 |

## 📁 Schema: `sbadcenter`

### 📄 Table: `cpc_billing`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `shop_number` | `varchar` | 가게 번호 |
| 2 | `shop_name` | `varchar` | 가게 이름 |
| 2 | `shop_owner_number` | `varchar` | 업주 번호 |
| 2 | `booking_id` | `varchar` | DH Central CPC 부킹 ID |
| 2 | `billing_date` | `date` | 과금일 |
| 2 | `central_billing_date` | `date` | DH Central 기준 과금일 |
| 2 | `billing_amount` | `double` | 과금액 ( 부가세  제외) |
| 2 | `click_count` | `bigint` | 집계된  클릭수 |
| 2 | `adjustment_required` | `tinyint` | 보정 요청 대상 여부 |
| 2 | `created_at` | `timestamp(9)` | 생성 일시 |
| 2 | `modified_at` | `timestamp(9)` | 수정 일시 |
| 2 | `shop_service_type` | `varchar` | 가게 서비스  유형 |
| 2 | `deleted` | `tinyint` | 삭제 여부 |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |

### 📄 Table: `ad_kind`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `id` | `varchar` | - |
| 1 | `advertiser_id` | `varchar` | - |
| 1 | `ad_inventory_id` | `varchar` | - |
| 1 | `title` | `varchar` | 상품 이름 |
| 1 | `ad_kind_key` | `varchar` | 상품의  유일성을  보장하는  키값(ex ULTRACALL88000) |
| 1 | `metadata` | `varchar` | 상품 메타데이터모든  광고들이  공통적으로  가질수도  안가질수도  있는 것들ex) 노출 카테고리  설정 가능여부 , 다른광고로  전환 기능 |
| 1 | `properties` | `varchar` | 상품 속성템플릿에  종속적인  데이터들이  저장된다 . 템플릿은  광고의  종류별로  다르다 . |
| 1 | `confirmed` | `tinyint` | 승인 여부 |
| 1 | `testing` | `tinyint` | 테스트용  상품 여부 |
| 1 | `sellable` | `tinyint` | 판매가능  여부 |
| 1 | `sellable_by_broker` | `tinyint` | 외부판매가능  여부 |
| 1 | `sell_begin_date` | `date` | 판매시작일자 |
| 1 | `sell_end_date` | `date` | 판매종료일자 |
| 1 | `supply_price` | `decimal(19,0)` | - |
| 1 | `commission_rate` | `decimal(7,4)` | 수수료율 |
| 1 | `commission_fixed_supply_price` | `decimal(19,0)` | - |
| 1 | `commission_special_rate` | `decimal(7,4)` | 우대 수수료율 |
| 1 | `commission_special_fixed_supply_price` | `decimal(19,0)` | - |
| 1 | `priority` | `double` | 노출 우선도 |
| 1 | `type` | `varchar` | 상품 타입 |
| 1 | `goal` | `varchar` | 상품 목표 타입 |
| 1 | `interval_days` | `varchar` | 과금 주기1:1 일, 7:1 주일, 14:2 주일, 30:1 개월, 60:2 개월, 90:3 개월, 180:6 개월, 365:1 년 |
| 1 | `default_auto_renew` | `tinyint` | 자동연장여부캠페인이  생성될때 , ad_campaign 테이블의  defaultAutoRenew 필드 기본값으로  사용됨 |
| 1 | `ui_template_key` | `varchar` | 템플릿의  키값새로운  광고 상품 또는 켐페인을  생성할때 , 광고의  종류별로  화면에서  보여져야하는  생성화면  템플릿이  존재한다 . 그 템플릿에  대한 키값을  저장한다 . |
| 1 | `unique_instance_key` | `varchar` | 상호 베타적으로  진행해야하는  광고를  위한 프로퍼티업소는  진행하려는  광고의  UniqueInstanceKey 값이 이미 진행중인  광고들의  uniqueInstanceKey 값들 중에 존재한다면 , 광고를  진행할  수 없다. |
| 1 | `cost_type` | `varchar` | 예산 타입BIZMONEY, BIZMONEY_DIRECT, RELATE, BAROPAY, BUDGET |
| 1 | `connected_shop_type` | `varchar` | - |
| 1 | `deleted` | `tinyint` | 삭제여부 |
| 1 | `created_at` | `timestamp(9)` | 생성일시 |
| 1 | `created_by_type` | `varchar` | 생성자  타입 |
| 1 | `created_by_id` | `varchar` | 생성자  id |
| 1 | `created_by_name` | `varchar` | 생성자  이름 |
| 1 | `modified_at` | `timestamp(9)` | 수정일시 |
| 1 | `modified_by_type` | `varchar` | 수정자  타입 |
| 1 | `modified_by_id` | `varchar` | 수정자  id |
| 1 | `modified_by_name` | `varchar` | 수정자  이름 |
| 1 | `ad_kind_group` | `varchar` | 상품을  그룹화  할수 있는 키 |
| 1 | `daily_supply_price` | `decimal(19,0)` | - |

## 📁 Schema: `dsdw`

### 📄 Table: `member_master`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `mem_no` | `varchar` | 배민회원번호 |
| 1 | `mem_id` | `varchar` | 회원 아이디 |
| 1 | `ci_seq` | `varchar` | CI SEQ |
| 1 | `gender` | `varchar` | 성별 |
| 1 | `age` | `integer` | 나이 |
| 1 | `birth_dt` | `varchar` | 생일 |
| 1 | `is_foreigner` | `tinyint` | 외국인여부 |
| 1 | `is_own_certificate` | `tinyint` | 본인 인증 여부 |
| 1 | `is_email_receive` | `tinyint` | 이메일  수신동의  여부 |
| 1 | `is_sms_receive` | `tinyint` | 문자 수신동의  여부 |
| 1 | `is_apppush_receive` | `tinyint` | APPPush 동의 여부 |
| 1 | `is_background_receive` | `tinyint` | 기기푸시  동의 여부 |
| 1 | `is_baeminpay_use` | `tinyint` | 배민페이  등록 여부 |
| 1 | `is_multidevice_use` | `tinyint` | 멀티 기기 사용 여부 |
| 1 | `is_employee` | `tinyint` | 임직원  여부 |
| 1 | `is_abuser` | `tinyint` | 어뷰저  여부 |
| 1 | `grade_cd` | `varchar` | 회원등급코드  (F/O - 2025-05-12) |
| 1 | `previous_grade_cd` | `varchar` | 이전회원등급코드  (F/O - 2025-05-12) |
| 1 | `grade_maintain_period_month` | `integer` | 회원등급유지개월수  (F/O - 2025-05-12) |
| 1 | `join_dt` | `varchar` | 가입일자 |
| 1 | `is_active` | `tinyint` | 활동 여부 |
| 1 | `is_leave` | `tinyint` | 탈퇴 여부 |
| 1 | `leave_dt` | `varchar` | 탈퇴 일자 |
| 1 | `leave_dttm` | `timestamp(9)` | 탈퇴 일시 |
| 1 | `is_dormancy` | `tinyint` | 휴면 여부 |
| 1 | `dormancy_dt` | `varchar` | 휴면 일자 |
| 1 | `dormancy_return_dt` | `varchar` | 휴면 복귀 일자 |
| 1 | `last_login_dt` | `varchar` | 마지막  로그인  일자 |
| 1 | `family_id` | `varchar` | 가족계정  아이디 |
| 1 | `first_provider_type` | `varchar` | 회원별  최초로그인수단 |
| 1 | `first_provider_sub_type` | `varchar` | 회원별  최초인증수단타입 |
| 1 | `is_bmclub_mbrshp_subs` | `tinyint` | 배민클럽멤버십구독여부 |
| 1 | `bmclub_mbrshp_status_cd` | `varchar` | 배민클럽멤버십상태코드 |
| 1 | `bmclub_mbrshp_subs_dttm` | `timestamp(9)` | 배민클럽멤버십구독일시 |
| 1 | `bmclub_mbrshp_expire_dt` | `date` | 배민클럽멤버십만료일자 |
| 1 | `next_bmclub_mbrshp_subs_pay_dt` | `date` | 다음배민클럽멤버십구독결제일자 |
| 1 | `first_bmclub_mbrshp_subs_dt` | `date` | 최초배민클럽멤버십구독일자 |
| 1 | `first_bmclub_mbrshp_paid_subs_dt` | `date` | 최초배민클럽멤버십유료구독일자 |
| 1 | `bmclub_mbrshp_subs_cnt` | `bigint` | 배민클럽멤버십구독수 |
| 1 | `bmclub_mbrshp_paid_subs_cnt` | `bigint` | 배민클럽멤버십유료구독수 |
| 1 | `bmclub_mbrshp_id` | `varchar` | 배민클럽멤버십 ID |
| 1 | `bmclub_mbrshp_end_dttm` | `timestamp(9)` | 배민클럽멤버십종료일시 |
| 1 | `is_bmclub_mbrshp_paid` | `tinyint` | 배민클럽멤버십유료여부 |
| 1 | `is_bizmem` | `tinyint` | 비즈회원여부 |
| 1 | `is_seller` | `tinyint` | 판매자여부 |
| 1 | `is_age14_under` | `tinyint` | 14 세미만여부 |
| 1 | `is_adult` | `tinyint` | 성인여부 |
| 1 | `bmclub_mbrshp_product_cd` | `varchar` | 배민클럽멤버십상품코드 |
| 1 | `mem_no` | `varchar` | 배민회원번호 |
| 1 | `mem_id` | `varchar` | 회원 아이디 |
| 1 | `ci_seq` | `varchar` | CI SEQ |
| 1 | `gender` | `varchar` | 성별 |
| 1 | `age` | `integer` | 나이 |
| 1 | `birth_dt` | `varchar` | 생일 |
| 1 | `is_foreigner` | `tinyint` | 외국인여부 |
| 1 | `is_own_certificate` | `tinyint` | 본인 인증 여부 |
| 1 | `is_email_receive` | `tinyint` | 이메일  수신동의  여부 |
| 1 | `is_sms_receive` | `tinyint` | 문자 수신동의  여부 |
| 1 | `is_apppush_receive` | `tinyint` | APPPush 동의 여부 |
| 1 | `is_background_receive` | `tinyint` | 기기푸시  동의 여부 |
| 1 | `is_baeminpay_use` | `tinyint` | 배민페이  등록 여부 |
| 1 | `is_multidevice_use` | `tinyint` | 멀티 기기 사용 여부 |
| 1 | `is_employee` | `tinyint` | 임직원  여부 |
| 1 | `is_abuser` | `tinyint` | 어뷰저  여부 |
| 1 | `grade_cd` | `varchar` | 회원등급코드  (F/O - 2025-05-12) |
| 1 | `previous_grade_cd` | `varchar` | 이전회원등급코드  (F/O - 2025-05-12) |
| 1 | `grade_maintain_period_month` | `integer` | 회원등급유지개월수  (F/O - 2025-05-12) |
| 1 | `join_dt` | `varchar` | 가입일자 |
| 1 | `is_active` | `tinyint` | 활동 여부 |
| 1 | `is_leave` | `tinyint` | 탈퇴 여부 |
| 1 | `leave_dt` | `varchar` | 탈퇴 일자 |
| 1 | `leave_dttm` | `timestamp(9)` | 탈퇴 일시 |
| 1 | `is_dormancy` | `tinyint` | 휴면 여부 |
| 1 | `dormancy_dt` | `varchar` | 휴면 일자 |
| 1 | `dormancy_return_dt` | `varchar` | 휴면 복귀 일자 |
| 1 | `last_login_dt` | `varchar` | 마지막  로그인  일자 |
| 1 | `family_id` | `varchar` | 가족계정  아이디 |
| 1 | `first_provider_type` | `varchar` | 회원별  최초로그인수단 |
| 1 | `first_provider_sub_type` | `varchar` | 회원별  최초인증수단타입 |
| 1 | `is_bmclub_mbrshp_subs` | `tinyint` | 배민클럽멤버십구독여부 |
| 1 | `bmclub_mbrshp_status_cd` | `varchar` | 배민클럽멤버십상태코드 |
| 1 | `bmclub_mbrshp_subs_dttm` | `timestamp(9)` | 배민클럽멤버십구독일시 |
| 1 | `bmclub_mbrshp_expire_dt` | `date` | 배민클럽멤버십만료일자 |
| 1 | `next_bmclub_mbrshp_subs_pay_dt` | `date` | 다음배민클럽멤버십구독결제일자 |
| 1 | `first_bmclub_mbrshp_subs_dt` | `date` | 최초배민클럽멤버십구독일자 |
| 1 | `first_bmclub_mbrshp_paid_subs_dt` | `date` | 최초배민클럽멤버십유료구독일자 |
| 1 | `bmclub_mbrshp_subs_cnt` | `bigint` | 배민클럽멤버십구독수 |
| 1 | `bmclub_mbrshp_paid_subs_cnt` | `bigint` | 배민클럽멤버십유료구독수 |
| 1 | `bmclub_mbrshp_id` | `varchar` | 배민클럽멤버십 ID |
| 1 | `bmclub_mbrshp_end_dttm` | `timestamp(9)` | 배민클럽멤버십종료일시 |
| 1 | `is_bmclub_mbrshp_paid` | `tinyint` | 배민클럽멤버십유료여부 |
| 1 | `is_bizmem` | `tinyint` | 비즈회원여부 |
| 1 | `is_seller` | `tinyint` | 판매자여부 |
| 1 | `is_age14_under` | `tinyint` | 14 세미만여부 |
| 1 | `is_adult` | `tinyint` | 성인여부 |
| 1 | `bmclub_mbrshp_product_cd` | `varchar` | 배민클럽멤버십상품코드 |

### 📄 Table: `menu_master_daily`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `menu_id` | `varchar` | 메뉴id |
| 2 | `menu_info_id` | `varchar` | 메뉴 기본정보  id |
| 2 | `menu_name` | `varchar` | 메뉴명 |
| 2 | `menu_name_clean` | `varchar` | 보정 메뉴명 |
| 2 | `menu_type` | `varchar` | 메뉴 타입 |
| 2 | `menu_display_order` | `integer` | 메뉴 정렬 순서 |
| 2 | `menu_group_id` | `varchar` | 메뉴 그룹 id |
| 2 | `menu_group_name` | `varchar` | 메뉴 그룹명 |
| 2 | `menu_group_desc` | `varchar` | 메뉴 그룹 설명 |
| 2 | `menu_group_display_order` | `integer` | 메뉴 그룹 정렬 순서 |
| 2 | `menupan_id` | `varchar` | 메뉴판  id |
| 2 | `menupan_name` | `varchar` | 메뉴판명 |
| 2 | `menupan_type` | `varchar` | 메뉴판  타입 |
| 2 | `is_menupan_displayed` | `tinyint` | 노출 메뉴판  여부 |
| 2 | `shop_no` | `varchar` | 가게번호 |
| 2 | `shop_service_type` | `varchar` | 가게 서비스타입 |
| 2 | `shop_category` | `varchar` | 가게 카테고리 |
| 2 | `shop_rgn3_cd` | `varchar` | 가게 지역코드 |
| 2 | `shop_status` | `varchar` | 가게 상태 |
| 2 | `is_franchise_shop` | `tinyint` | 프랜차이즈  가게 여부 |
| 2 | `franchise_no` | `varchar` | 프랜차이즈  번호 |
| 2 | `is_franchise_menupan` | `tinyint` | 프랜차이즈  메뉴판  여부 |
| 2 | `franchise_manage_type` | `varchar` | 프랜차이즈  관리 타입 |
| 2 | `is_franchise_menu` | `tinyint` | 프랜차이즈  메뉴 여부 |
| 2 | `franchise_menu_id` | `varchar` | 프랜차이즈  메뉴 id |
| 2 | `menu_price_count` | `integer` | 메뉴 가격수 |
| 2 | `menu_price_min` | `integer` | 최소 메뉴 가격 |
| 2 | `menu_price_max` | `integer` | 최대 메뉴 가격 |
| 2 | `menu_price_type` | `varchar` | 메뉴 가격 타입 |
| 2 | `menu_simple_desc` | `varchar` | 메뉴 구성 설명 |
| 2 | `menu_desc` | `varchar` | 메뉴 설명 |
| 2 | `menu_category` | `varchar` | 메뉴 카테고리 |
| 2 | `menu_tag` | `varchar` | 메뉴 태그 |
| 2 | `nutrient` | `varchar` | 영양 성분 |
| 2 | `allergy` | `varchar` | 알러지  성분 |
| 2 | `is_vegetarian` | `tinyint` | 채식메뉴  여부 |
| 2 | `vegetarian_menu_attr` | `varchar` | 채식메뉴  속성 |
| 2 | `is_image` | `tinyint` | 이미지  등록 여부 |
| 2 | `image_count` | `integer` | 이미지  수 |
| 2 | `is_representative` | `tinyint` | 대표메뉴  여부 |
| 2 | `is_popular` | `tinyint` | 인기메뉴  여부 |
| 2 | `is_solo` | `tinyint` | 1 인분메뉴  여부 |
| 2 | `is_alcohol` | `tinyint` | 주류 여부 |
| 2 | `is_menu_soldout` | `tinyint` | 메뉴 품절 여부 |
| 2 | `restocked_dttm` | `timestamp(9)` | 품절 해제 일시(UTC) |
| 2 | `is_menu_displayed` | `tinyint` | 메뉴 노출 여부 |
| 2 | `is_menu_deleted` | `tinyint` | 메뉴 삭제 여부 ( 메뉴, 메뉴 기본정보 , 메뉴 그룹, 메뉴판  테이블에서  하나라도  삭제 되었을경우  삭제(1) 로 조회됩니다 ) |
| 2 | `created_dttm` | `timestamp(9)` | 메뉴 등록일시 (UTC) |
| 2 | `modified_dttm` | `timestamp(9)` | 메뉴 수정일시 (UTC) |
| 2 | `is_menu_table_deleted` | `tinyint` | 메뉴 삭제 여부 ( 메뉴 테이블 ) |
| 2 | `is_menu_group_displayed` | `tinyint` | 메뉴 그룹 노출 여부 |
| 2 | `is_menu_group_deleted` | `tinyint` | 메뉴 그룹 삭제 여부 |
| 2 | `is_promo_discount` | `tinyint` | 대상이  프로모션으로  할인을  적용 받았는  지 여부를  저장(1: 적용, 0: 미적용 ) |
| 2 | `menu_promo_id` | `varchar` | 메뉴 할인에  적용된  메뉴프로모션  ID 값을 저장 |
| 2 | `menu_promo_type_cd` | `varchar` | 메뉴 할인시  적용된  프로모션의  유형을  코드로  저장(MENU_MFO, MENU_NORMAL) |
| 2 | `menu_promo_discount_amt` | `bigint` | 메뉴 프로모션으로  적용된  할인금액을  저장( 정액할인은  할인금액  그대로 , 정률할인은  금액으로  변환되어  저장) |
| 2 | `is_beverage` | `tinyint` | 대상이  음료인지  여부 정보를  저장(1: 음료, 0: 음료아님 ) |
| 2 | `min_offline_menu_price` | `integer` | 최소오프라인메뉴가격 |
| 2 | `max_offline_menu_price` | `integer` | 최대오프라인메뉴가격 |
| 2 | `min_takeout_menu_price` | `integer` | 최소포장메뉴가격 |
| 2 | `max_takeout_menu_price` | `integer` | 최대포장메뉴가격 |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `cl_epm`

### 📄 Table: `member_first_order_master`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `mem_no` | `varchar` | 회원 번호 |
| 1 | `brs_mem_no` | `varchar` | 배민상회  회원번호 |
| 1 | `first_ord_no` | `varchar` | 첫 주문 번호 |
| 1 | `first_ord_dt` | `varchar` | 첫 주문 일자 |
| 1 | `first_ord_dttm` | `timestamp(9)` | 첫 주문 일시 |
| 1 | `first_ord_price` | `integer` | 첫 주문 금액 |
| 1 | `last_ord_no` | `varchar` | 마지막  주문 번호 |
| 1 | `last_ord_dt` | `varchar` | 마지막  주문 일자 |
| 1 | `last_ord_dttm` | `timestamp(9)` | 마지막  주문 일시 |
| 1 | `last_ord_price` | `integer` | 마지막  주문 금액 |
| 1 | `tot_ord_amt` | `bigint` | 총 주문 금액 |
| 1 | `tot_ord_cnt` | `integer` | 총 주문 수 |
| 1 | `is_reord` | `tinyint` | 재 주문 여부 |
| 1 | `days_since_last_ord` | `integer` | 미 주문 소요 일수 |
| 1 | `created_at` | `timestamp(9)` | 생성일시 |
| 1 | `svc_cd` | `varchar` | **[파티션 키]** 서비스  코드 |
| 1 | `mem_no` | `varchar` | 회원 번호 |
| 1 | `brs_mem_no` | `varchar` | 배민상회  회원번호 |
| 1 | `first_ord_no` | `varchar` | 첫 주문 번호 |
| 1 | `first_ord_dt` | `varchar` | 첫 주문 일자 |
| 1 | `first_ord_dttm` | `timestamp(9)` | 첫 주문 일시 |
| 1 | `first_ord_price` | `integer` | 첫 주문 금액 |
| 1 | `last_ord_no` | `varchar` | 마지막  주문 번호 |
| 1 | `last_ord_dt` | `varchar` | 마지막  주문 일자 |
| 1 | `last_ord_dttm` | `timestamp(9)` | 마지막  주문 일시 |
| 1 | `last_ord_price` | `integer` | 마지막  주문 금액 |
| 1 | `tot_ord_amt` | `bigint` | 총 주문 금액 |
| 1 | `tot_ord_cnt` | `integer` | 총 주문 수 |
| 1 | `is_reord` | `tinyint` | 재 주문 여부 |
| 1 | `days_since_last_ord` | `integer` | 미 주문 소요 일수 |
| 1 | `created_at` | `timestamp(9)` | 생성일시 |
| 1 | `svc_cd` | `varchar` | **[파티션 키]** 서비스  코드 |

## 📁 Schema: `sbadcenter_hist`

### 📄 Table: `ad_campaign_master`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `ad_campaign_id` | `varchar` | 광고캠페인  ID |
| 1 | `ad_kind_id` | `varchar` | 광고상품  ID |
| 1 | `ad_kind_title` | `varchar` | 광고상품  이름 |
| 1 | `ad_kind_group` | `varchar` | 상품 그룹화  할수 있는 키 |
| 1 | `ad_inventory_id` | `varchar` | 광고인벤토리  ID |
| 1 | `inventory_type` | `varchar` | 인벤토리  종류 |
| 1 | `inventory_name` | `varchar` | 인벤토리  이름 |
| 1 | `inventory_key` | `varchar` | 인벤토리  키 |
| 1 | `shop_no` | `varchar` | 가게번호 |
| 1 | `shop_owner_no` | `varchar` | 업주번호 |
| 1 | `service_begin_datetime` | `timestamp(9)` | 실제 서비스  시작 일시 |
| 1 | `service_end_datetime` | `timestamp(9)` | 실제 서비스  종료 일시 |
| 1 | `ad_ongoing_days` | `varchar` | 광고가  진행된  일 수 |
| 1 | `total_capacity` | `bigint` | 총 목표 도달 횟수 제한 |
| 1 | `daily_capacity` | `bigint` | 일일 목표 도달 횟수 제한 |
| 1 | `adaddress` | `varchar` | 광고주소 |
| 1 | `is_ongoing` | `tinyint` | 광고 노출 여부 |
| 1 | `is_ad_active` | `tinyint` | 광고 진행 여부 |
| 1 | `is_ad_paused` | `tinyint` | 일시중지  여부 |
| 1 | `is_ad_finished` | `tinyint` | 광고 캠페인  종료 여부 |
| 1 | `is_ad_deleted` | `tinyint` | 삭제 여부 |
| 1 | `is_auto_renew` | `tinyint` | 자동 갱신 여부 |
| 1 | `is_test` | `tinyint` | 테스트  광고 여부 |
| 1 | `ad_category` | `varchar` | 광고 카테고리  ( 배민에만  해당) |
| 1 | `display_categories` | `array(varchar)` | 노출 카테고리  ( 배민은  1:1, 배라는  1:N) |
| 1 | `subdisplay_categories` | `array(varchar)` | 배라 서브 노출 카테고리 |
| 1 | `franchise_no` | `varchar` | 프랜차이즈  번호 |
| 1 | `franchise_name` | `varchar` | 프랜차이즈  이름 |
| 1 | `latitude` | `varchar` | geometry 위도 정보 |
| 1 | `longitude` | `varchar` | geometry 경도 정보 |
| 1 | `shop_rgn1_cd` | `varchar` | 가게 지역 1 코드 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 1 | `shop_rgn2_cd` | `varchar` | 가게 지역 2 코드 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 1 | `shop_rgn3_cd` | `varchar` | 가게 지역 3 코드 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 1 | `shop_rgn1_name` | `varchar` | 가게 지역 1 명칭 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 1 | `shop_rgn2_name` | `varchar` | 가게 지역 2 명칭 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 1 | `shop_rgn3_name` | `varchar` | 가게 지역 3 명칭 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 1 | `dsm_no` | `varchar` | DSM 번호 |
| 1 | `dsm_name` | `varchar` | DSM 이름 |
| 1 | `dsm_type` | `varchar` | DSM 타입코드 |
| 1 | `manager_no` | `varchar` | 매니저  번호 |
| 1 | `company_no` | `varchar` | 기업번호  ( 상호번호 ) |
| 1 | `head_office_company_no` | `varchar` | 최상위  회사 번호 |
| 1 | `company_type` | `varchar` | 기업 구분 코드 |
| 1 | `company_name` | `varchar` | 기업명 |
| 1 | `commission_rate` | `double` | 수수료율 |
| 1 | `commission_fixed_supply_price` | `bigint` | 건당 수수료금액 |
| 1 | `is_theme` | `tinyint` | 오픈리스트  광고 중 1 인분, 채식 등 테마광고  노출 여부 |
| 1 | `is_takeout` | `tinyint` | 테이크아웃  가능 여부 |
| 1 | `is_eatin` | `tinyint` | 매장 식사 가능 여부 |
| 1 | `created_at` | `timestamp(9)` | 생성일시 |
| 1 | `modified_at` | `timestamp(9)` | 수정일시 |
| 1 | `data` | `varchar` | 기타 정보 |
| 1 | `shop_status` | `varchar` | 가게 상태 |
| 1 | `is_test_seller` | `tinyint` | 테스트  업주 여부 |
| 1 | `is_test_shop` | `tinyint` | 테스트  shop 여부 |
| 1 | `is_test_dsm` | `tinyint` | 테스트  dsm 여부 |
| 1 | `is_bmclub` | `tinyint` | 배민클럽  여부 |
| 1 | `part_date` | `varchar` | **[파티션 키]**  |
| 2 | `ad_campaign_id` | `varchar` | 광고캠페인  ID |
| 2 | `ad_kind_id` | `varchar` | 광고상품  ID |
| 2 | `ad_kind_title` | `varchar` | 광고상품  이름 |
| 2 | `ad_kind_group` | `varchar` | 상품 그룹화  할수 있는 키 |
| 2 | `ad_inventory_id` | `varchar` | 광고인벤토리  ID |
| 2 | `inventory_type` | `varchar` | 인벤토리  종류 |
| 2 | `inventory_name` | `varchar` | 인벤토리  이름 |
| 2 | `inventory_key` | `varchar` | 인벤토리  키 |
| 2 | `shop_no` | `varchar` | 가게번호 |
| 2 | `shop_owner_no` | `varchar` | 업주번호 |
| 2 | `service_begin_datetime` | `timestamp(9)` | 실제 서비스  시작 일시 |
| 2 | `service_end_datetime` | `timestamp(9)` | 실제 서비스  종료 일시 |
| 2 | `ad_ongoing_days` | `varchar` | 광고가  진행된  일 수 |
| 2 | `total_capacity` | `bigint` | 총 목표 도달 횟수 제한 |
| 2 | `daily_capacity` | `bigint` | 일일 목표 도달 횟수 제한 |
| 2 | `adaddress` | `varchar` | 광고주소 |
| 2 | `is_ongoing` | `tinyint` | 광고 노출 여부 |
| 2 | `is_ad_active` | `tinyint` | 광고 진행 여부 |
| 2 | `is_ad_paused` | `tinyint` | 일시중지  여부 |
| 2 | `is_ad_finished` | `tinyint` | 광고 캠페인  종료 여부 |
| 2 | `is_ad_deleted` | `tinyint` | 삭제 여부 |
| 2 | `is_auto_renew` | `tinyint` | 자동 갱신 여부 |
| 2 | `is_test` | `tinyint` | 테스트  광고 여부 |
| 2 | `ad_category` | `varchar` | 광고 카테고리  ( 배민에만  해당) |
| 2 | `display_categories` | `array(varchar)` | 노출 카테고리  ( 배민은  1:1, 배라는  1:N) |
| 2 | `subdisplay_categories` | `array(varchar)` | 배라 서브 노출 카테고리 |
| 2 | `franchise_no` | `varchar` | 프랜차이즈  번호 |
| 2 | `franchise_name` | `varchar` | 프랜차이즈  이름 |
| 2 | `latitude` | `varchar` | geometry 위도 정보 |
| 2 | `longitude` | `varchar` | geometry 경도 정보 |
| 2 | `shop_rgn1_cd` | `varchar` | 가게 지역 1 코드 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 2 | `shop_rgn2_cd` | `varchar` | 가게 지역 2 코드 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 2 | `shop_rgn3_cd` | `varchar` | 가게 지역 3 코드 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 2 | `shop_rgn1_name` | `varchar` | 가게 지역 1 명칭 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 2 | `shop_rgn2_name` | `varchar` | 가게 지역 2 명칭 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 2 | `shop_rgn3_name` | `varchar` | 가게 지역 3 명칭 ( 법정동  전환 기간 : 2019-04-01 ~) |
| 2 | `dsm_no` | `varchar` | DSM 번호 |
| 2 | `dsm_name` | `varchar` | DSM 이름 |
| 2 | `dsm_type` | `varchar` | DSM 타입코드 |
| 2 | `manager_no` | `varchar` | 매니저  번호 |
| 2 | `company_no` | `varchar` | 기업번호  ( 상호번호 ) |
| 2 | `head_office_company_no` | `varchar` | 최상위  회사 번호 |
| 2 | `company_type` | `varchar` | 기업 구분 코드 |
| 2 | `company_name` | `varchar` | 기업명 |
| 2 | `commission_rate` | `double` | 수수료율 |
| 2 | `commission_fixed_supply_price` | `bigint` | 건당 수수료금액 |
| 2 | `is_theme` | `tinyint` | 오픈리스트  광고 중 1 인분, 채식 등 테마광고  노출 여부 |
| 2 | `is_takeout` | `tinyint` | 테이크아웃  가능 여부 |
| 2 | `is_eatin` | `tinyint` | 매장 식사 가능 여부 |
| 2 | `created_at` | `timestamp(9)` | 생성일시 |
| 2 | `modified_at` | `timestamp(9)` | 수정일시 |
| 2 | `data` | `varchar` | 기타 정보 |
| 2 | `shop_status` | `varchar` | 가게 상태 |
| 2 | `is_test_seller` | `tinyint` | 테스트  업주 여부 |
| 2 | `is_test_shop` | `tinyint` | 테스트  shop 여부 |
| 2 | `is_test_dsm` | `tinyint` | 테스트  dsm 여부 |
| 2 | `is_bmclub` | `tinyint` | 배민클럽  여부 |
| 2 | `part_date` | `varchar` | **[파티션 키]**  |

## 📁 Schema: `sbstore`

### 📄 Table: `shop_owner_v2`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 2 | `shop_owner_no` | `varchar` | 업주 번호 |
| 2 | `customer_no` | `varchar` | 고객번호 |
| 2 | `member_no` | `varchar` | 회원번호 |
| 2 | `shop_owner_name` | `varchar` | 업주명 ( 상호명 ) |
| 2 | `business_no` | `varchar` | 사업자  번호 |
| 2 | `sub_business_no` | `varchar` | 종사업장  번호 |
| 2 | `business_type` | `varchar` | 업종 |
| 2 | `business_item` | `varchar` | 업태 |
| 2 | `corporation_registration_no` | `varchar` | 법인등록번호 |
| 2 | `grade` | `varchar` | 업주 등급 |
| 2 | `status` | `varchar` | 업주 상태 |
| 2 | `co_ceo` | `tinyint` | 공동대표  여부 |
| 2 | `member_connected` | `tinyint` | B2B 통합회원  연동여부 |
| 2 | `zip_code` | `varchar` | 우편번호 |
| 2 | `new_zip_code` | `varchar` | ( 신) 우편번호 |
| 2 | `deleted_date` | `timestamp(9)` | 업주 삭제 일자 |
| 2 | `is_deleted` | `tinyint` | 업주 삭제 여부 |
| 2 | `is_test` | `tinyint` | 테스트  업주 여부 |
| 2 | `registered` | `timestamp(9)` | 등록 일자 |
| 2 | `modified` | `timestamp(9)` | 수정 일자 |
| 2 | `address` | `varchar` | 지번주소 |
| 2 | `address_detail` | `varchar` | 지번주소  상세 |
| 2 | `road_address` | `varchar` | 도로명주소 |
| 2 | `road_address_detail` | `varchar` | 도로명주소  상세 |

## 📁 Schema: `membership`

### 📄 Table: `member`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `id` | `varchar` | 식별자 |
| 1 | `member_number` | `varchar` | 회원번호 |
| 1 | `membership_status` | `varchar` | 멤버십  상태 |
| 1 | `tx_date_time` | `timestamp(9)` | 멤버십  상태 최종 상태 변경 일시 |
| 1 | `version` | `bigint` | 낙관적  락 버전 |
| 1 | `created_datetime` | `timestamp(9)` | 데이터  생성 일시 |
| 1 | `modified_datetime` | `timestamp(9)` | 데이터  수정 일시 |

### 📄 Table: `subscribe_hist`

| 중요도 | 컬럼명 | 데이터타입 | 설명 (비즈니스 로직) |
| :---: | :--- | :--- | :--- |
| 1 | `id` | `varchar` | 식별자 |
| 1 | `member_id` | `varchar` | member 테이블의  식별자 |
| 1 | `membership_code` | `varchar` | 상품 코드 |
| 1 | `promotion_group_types` | `varchar` | 지급 받은 프로모션  그룹 |
| 1 | `start_date_time` | `timestamp(9)` | 구독 시작일 |
| 1 | `end_date` | `date` | 구독 종료일 |
| 1 | `recurrent_number` | `varchar` | 정기결제  번호 |
| 1 | `created_datetime` | `timestamp(9)` | 데이터  생성 일시 |
| 1 | `modified_datetime` | `timestamp(9)` | 데이터  수정 일시 |
| 1 | `region` | `varchar` | 구독 지역 코드 ( 법정동 ) |
| 1 | `next_payment_date` | `date` | 다음 유료 결제일 |
| 1 | `group_key` | `varchar` | 멤버십  회차 그룹 키 |
| 1 | `part_date` | `varchar` | **[파티션 키]**  |


배민클럽 멤버십 고객 관련 테이블

dsdw.member_master_daily
Column	Type	Extra	Comment
mem_no	varchar		배민회원번호
mem_id	varchar		회원 아이디
ci_seq	varchar		CI SEQ
gender	varchar		성별
age	integer		나이
birth_dt	varchar		생일
is_foreigner	tinyint		외국인여부
is_own_certificate	tinyint		본인 인증 여부
is_email_receive	tinyint		이메일 수신동의 여부
is_sms_receive	tinyint		문자 수신동의 여부
is_apppush_receive	tinyint		APPPush 동의 여부
is_background_receive	tinyint		기기푸시 동의 여부
is_baeminpay_use	tinyint		배민페이 등록 여부
is_multidevice_use	tinyint		멀티 기기 사용 여부
is_employee	tinyint		임직원 여부
is_abuser	tinyint		어뷰저 여부
grade_cd	varchar		회원등급코드 (F/O - 2025-05-12)
previous_grade_cd	varchar		이전회원등급코드 (F/O - 2025-05-12)
grade_maintain_period_month	integer		회원등급유지개월수 (F/O - 2025-05-12)
join_dt	varchar		가입일자
is_active	tinyint		활동 여부
is_leave	tinyint		탈퇴 여부
leave_dt	varchar		탈퇴 일자
leave_dttm	timestamp(9)		탈퇴 일시
is_dormancy	tinyint		휴면 여부
dormancy_dt	varchar		휴면 일자
dormancy_return_dt	varchar		휴면 복귀 일자
last_login_dt	varchar		마지막 로그인 일자
family_id	varchar		가족계정 아이디
first_provider_type	varchar		회원별 최초로그인수단
first_provider_sub_type	varchar		회원별 최초인증수단타입
is_bmclub_mbrshp_subs	tinyint		배민클럽멤버십구독여부
bmclub_mbrshp_status_cd	varchar		배민클럽멤버십상태코드
bmclub_mbrshp_subs_dttm	timestamp(9)		배민클럽멤버십구독일시
bmclub_mbrshp_expire_dt	date		배민클럽멤버십만료일자
next_bmclub_mbrshp_subs_pay_dt	date		다음배민클럽멤버십구독결제일자
first_bmclub_mbrshp_subs_dt	date		최초배민클럽멤버십구독일자
first_bmclub_mbrshp_paid_subs_dt	date		최초배민클럽멤버십유료구독일자
bmclub_mbrshp_subs_cnt	bigint		배민클럽멤버십구독수
bmclub_mbrshp_paid_subs_cnt	bigint		배민클럽멤버십유료구독수
bmclub_mbrshp_id	varchar		배민클럽멤버십ID
bmclub_mbrshp_end_dttm	timestamp(9)		배민클럽멤버십종료일시
is_bmclub_mbrshp_paid	tinyint		배민클럽멤버십유료여부
is_bizmem	tinyint		비즈회원여부
is_seller	tinyint		판매자여부
is_age14_under	tinyint		14세미만여부
is_adult	tinyint		성인여부
bmclub_mbrshp_product_cd	varchar		배민클럽멤버십상품코드
part_date	varchar	partition key	


dsdw.bmclub_mbrshp_master

Column	Type	Extra	Comment
bmclub_mbrshp_id	varchar		배민클럽멤버십ID
bmclub_mbrshp_product_cd	varchar		배민클럽멤버십상품코드
bmclub_mbrshp_status_cd	varchar		배민클럽멤버십상태코드
mem_no	varchar		회원번호
bmclub_mbrshp_start_dttm	timestamp(9)		배민클럽멤버십시작일시
bmclub_mbrshp_expire_dt	date		배민클럽멤버십만료예정일자
bmclub_mbrshp_end_dttm	timestamp(9)		배민클럽멤버십종료일시
next_bmclub_mbrshp_subs_pay_dt	date		배민클럽멤버십다음결제일자
bmclub_mbrshp_product_amt	bigint		배민클럽멤버십상품금액
bmclub_mbrshp_discount_amt	bigint		배민클럽멤버십할인금액
bmclub_mbrshp_pay_amt	bigint		배민클럽멤버십결제금액
is_bmclub_mbrshp_paid	tinyint		배민클럽멤버십유료여부
bmclub_mbrshp_rgn3_cd	varchar		배민클럽멤버십지역소분류코드
is_test	tinyint		테스트여부
subs_aft_ddcnt	integer		구독이후일수
bmclub_subs_id	varchar		배민클럽구독ID
food_ord_cnt	bigint		푸드주문수
bmclub_benefit_food_ord_cnt	bigint		배민클럽혜택푸드주문수
part_date	varchar	partition key	파티션일자


cl_epm.ord_cust_benefit_info

Column	Type	Extra	Comment
ord_no	varchar		주문번호
ord_dttm	timestamp(6) with time zone		주문일시
mem_no	varchar		회원번호
brs_mem_no	varchar		배민상회회원번호
seller_shop_mapinfo	varchar		판매자가게매핑정보
dlvry_rgn_cd	varchar		배달지역코드
ord_rgn3_cd	varchar		주문지역소분류코드
is_mem_ord	integer		회원주문여부
is_stod	integer		알뜰배달여부
is_svc_first_ord	integer		서비스최초주문여부
is_bmapp_first_ord	integer		배민앱최초주문여부
is_mfo	integer		MFO여부
is_timesale	integer		시간한정할인여부
is_bmclub_mbrshp_subs	integer		배민클럽멤버십구독여부
is_bmclub	integer		배민클럽여부
ord_status_clsf_cd	varchar		주문상태분류코드
is_cmplt_ord	integer		완료주문여부
is_cancel	integer		취소여부
ord_amt	bigint		주문금액
small_order_fee	bigint		소액주문비
envelope_amt	bigint		봉투금액
org_dlvry_tip	bigint		원본배달팁
dlvry_tip	bigint		배달팁
base_dlvry_tip	bigint		기본배달팁
extra_dlvry_tip	bigint		할증배달팁
dlvry_tip_discount_amt	bigint		배달팁할인금액
other_dlvry_tip_discount_amt	bigint		기타배달팁할인금액
cust_benefit_amt	bigint		고객혜택금액
company_charge_amt	bigint		회사부담금액
seller_charge_amt	bigint		판매자부담금액
thrdprt_charge_amt	bigint		제3자부담금액
cpn_use_amt	bigint		쿠폰사용금액
discount_amt	bigint		할인금액
point_use_amt	bigint		포인트사용금액
menu_discount_amt	bigint		메뉴할인금액
takeout_discount_amt	bigint		포장할인금액
giftcard_purchase_discount_amt	bigint		상품권구매할인금액
emply_discount_amt	bigint		임직원할인금액
instdc_discount_amt	bigint		즉시할인할인금액
instdc_ord_discount_amt	bigint		즉시할인주문할인금액
instdc_dlvry_tip_discount_amt	bigint		즉시할인배달팁할인금액
company_charge_cpn_amt	bigint		회사부담쿠폰금액
company_charge_discount_amt	bigint		회사부담할인금액
company_charge_point_amt	bigint		회사부담포인트금액
company_charge_menu_discount_amt	bigint		회사부담메뉴할인금액
company_charge_takeout_discount_amt	bigint		회사부담포장할인금액
company_charge_giftcard_purchase_discount_amt	bigint		회사부담상품권구매할인금액
company_charge_emply_discount_amt	bigint		회사부담임직원할인금액
seller_charge_cpn_amt	bigint		판매자부담쿠폰금액
company_charge_instdc_ord_discount_amt	bigint		회사부담즉시할인주문할인금액
company_charge_instdc_dlvry_tip_discount_amt	bigint		회사부담즉시할인배달팁할인금액
company_charge_other_dlvry_tip_discount_amt	bigint		회사부담기타배달팁할인금액
seller_charge_discount_amt	bigint		판매자부담할인금액
seller_charge_menu_discount_amt	bigint		판매자부담메뉴할인금액
seller_charge_takeout_discount_amt	bigint		판매자부담포장할인금액
seller_charge_giftcard_purchase_discount_amt	bigint		판매자부담상품권구매할인금액
seller_charge_instdc_ord_discount_amt	bigint		판매자부담즉시할인주문할인금액
seller_charge_instdc_dlvry_tip_discount_amt	bigint		판매자부담즉시할인배달팁할인금액
seller_charge_other_dlvry_tip_discount_amt	bigint		판매자부담기타배달팁할인금액
thrdprt_charge_cpn_amt	bigint		제3자부담쿠폰금액
thrdprt_charge_giftcard_purchase_discount_amt	bigint		제3자부담상품권구매할인금액
thrdprt_charge_instdc_ord_discount_amt	bigint		제3자부담즉시할인주문할인금액
thrdprt_charge_instdc_dlvry_tip_discount_amt	bigint		제3자부담즉시할인배달팁할인금액
thrdprt_charge_other_dlvry_tip_discount_amt	bigint		제3자부담기타배달팁할인금액
part_svc_cd	varchar		파티션서비스코드
part_date	varchar		파티션일자

cl_epm.ord_cust_benefit_info       
Column	Type	Extra	Comment
ord_no	varchar		주문번호
ord_dttm	timestamp(6) with time zone		주문일시
mem_no	varchar		회원번호
brs_mem_no	varchar		배민상회회원번호
seller_shop_mapinfo	varchar		판매자가게매핑정보
dlvry_rgn_cd	varchar		배달지역코드
ord_rgn3_cd	varchar		주문지역소분류코드
is_mem_ord	integer		회원주문여부
is_stod	integer		알뜰배달여부
is_svc_first_ord	integer		서비스최초주문여부
is_bmapp_first_ord	integer		배민앱최초주문여부
is_mfo	integer		MFO여부
is_timesale	integer		시간한정할인여부
is_bmclub_mbrshp_subs	integer		배민클럽멤버십구독여부
is_bmclub	integer		배민클럽여부
ord_status_clsf_cd	varchar		주문상태분류코드
is_cmplt_ord	integer		완료주문여부
is_cancel	integer		취소여부
ord_amt	bigint		주문금액
small_order_fee	bigint		소액주문비
envelope_amt	bigint		봉투금액
org_dlvry_tip	bigint		원본배달팁
dlvry_tip	bigint		배달팁
base_dlvry_tip	bigint		기본배달팁
extra_dlvry_tip	bigint		할증배달팁
dlvry_tip_discount_amt	bigint		배달팁할인금액
other_dlvry_tip_discount_amt	bigint		기타배달팁할인금액
cust_benefit_amt	bigint		고객혜택금액
company_charge_amt	bigint		회사부담금액
seller_charge_amt	bigint		판매자부담금액
thrdprt_charge_amt	bigint		제3자부담금액
cpn_use_amt	bigint		쿠폰사용금액
discount_amt	bigint		할인금액
point_use_amt	bigint		포인트사용금액
menu_discount_amt	bigint		메뉴할인금액
takeout_discount_amt	bigint		포장할인금액
giftcard_purchase_discount_amt	bigint		상품권구매할인금액
emply_discount_amt	bigint		임직원할인금액
instdc_discount_amt	bigint		즉시할인할인금액
instdc_ord_discount_amt	bigint		즉시할인주문할인금액
instdc_dlvry_tip_discount_amt	bigint		즉시할인배달팁할인금액
company_charge_cpn_amt	bigint		회사부담쿠폰금액
company_charge_discount_amt	bigint		회사부담할인금액
company_charge_point_amt	bigint		회사부담포인트금액
company_charge_menu_discount_amt	bigint		회사부담메뉴할인금액
company_charge_takeout_discount_amt	bigint		회사부담포장할인금액
company_charge_giftcard_purchase_discount_amt	bigint		회사부담상품권구매할인금액
company_charge_emply_discount_amt	bigint		회사부담임직원할인금액
seller_charge_cpn_amt	bigint		판매자부담쿠폰금액
company_charge_instdc_ord_discount_amt	bigint		회사부담즉시할인주문할인금액
company_charge_instdc_dlvry_tip_discount_amt	bigint		회사부담즉시할인배달팁할인금액
company_charge_other_dlvry_tip_discount_amt	bigint		회사부담기타배달팁할인금액
seller_charge_discount_amt	bigint		판매자부담할인금액
seller_charge_menu_discount_amt	bigint		판매자부담메뉴할인금액
seller_charge_takeout_discount_amt	bigint		판매자부담포장할인금액
seller_charge_giftcard_purchase_discount_amt	bigint		판매자부담상품권구매할인금액
seller_charge_instdc_ord_discount_amt	bigint		판매자부담즉시할인주문할인금액
seller_charge_instdc_dlvry_tip_discount_amt	bigint		판매자부담즉시할인배달팁할인금액
seller_charge_other_dlvry_tip_discount_amt	bigint		판매자부담기타배달팁할인금액
thrdprt_charge_cpn_amt	bigint		제3자부담쿠폰금액
thrdprt_charge_giftcard_purchase_discount_amt	bigint		제3자부담상품권구매할인금액
thrdprt_charge_instdc_ord_discount_amt	bigint		제3자부담즉시할인주문할인금액
thrdprt_charge_instdc_dlvry_tip_discount_amt	bigint		제3자부담즉시할인배달팁할인금액
thrdprt_charge_other_dlvry_tip_discount_amt	bigint		제3자부담기타배달팁할인금액
part_svc_cd	varchar		파티션서비스코드
part_date	varchar		파티션일자                          


