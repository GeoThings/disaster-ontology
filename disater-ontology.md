| 災害類別 | 建議標籤 | 建議原因或來源 | 範例 | 附註 |
| :--- | :--- | :--- | :--- | :--- |
| **通用 (所有回報)** | `id` | 4W-COP 核心原則，為每筆觀測提供唯一識別碼，利於追蹤與關聯。 | `"a1b2c3d4-e5f6-g7h8-i9j0-k1l2m3n4o5p6"` | `String (UUID)`, **必要** |
| 通用 (所有回報) | `event_id` | 4W-COP 核心原則，將單筆觀測連結至一個宏觀的災害事件（如「海棠颱風」），是災情彙整的關鍵。 | `"typhoon-haitang-2024"` | `String`, **必要** |
| 通用 (所有回報) | `timestamp` | 4W-COP 核心原則 (When)，記錄事件發生或回報的精確時間。 | `"2024-08-15T14:30:00Z"` | `String (ISO 8601)`, **必要** |
| 通用 (所有回報) | `observation_type` | 核心本體論設計，定義觀測回報的性質，是所有分類的基礎。 | `"incident_report"` | `String`, **必要** |
| 通用 (所有回報) | `actor_id` | 4W-COP 核心原則 (Who)，標示資訊來源，有助於評估資訊可信度。 | `"citizen-uuid-xyz"` | `String`, **必要** |
| 通用 (所有回報) | `status` | 核心本體論設計，追蹤資訊的生命週期，避免重複處理。 | `"verified"` | `String`, Enum: `unverified`, `verified`, `in_progress`, `resolved`, `invalid` |
| 通用 (所有回報) | `source` | 核心本體論設計，記錄資訊的接收管道。 | `"citizen_app"` | `String`, Enum: `citizen_app`, `119_dispatch`, `social_media`, `field_surveyor` |
| **備災與演習** | `asset_type` | 盤點防救災資源與設施，對應災害管理「整備」階段需求。 | `"shelter"` | `String`, Enum: `shelter`, `resource_depot`, `hospital` |
| 備災與演習 | `emergency=disaster_response` | OSM 已批准的標準標籤，用於標示非軍事性質的民間災防單位據點（如德國 THW）。 | `emergency=disaster_response` | `Node or Area` |
| 備災與演習 | `emergency=assembly_point` | OSM 標準標籤，用於標示災時的緊急集合點。 | `emergency=assembly_point` | `Node or Area` |
| 備災與演習 | `assembly_point:[disaster_type]=yes` | OSM 命名空間標籤，用於指定緊急集合點對應的災害類型。 | `assembly_point:earthquake=yes` | `Boolean` |
| 備災與演習 | `social_facility=shelter` | OSM 常用標籤，用於標示避難收容所，可搭配 `emergency:*` 命名空間使用。 | `social_facility=shelter` | `Node or Area` |
| 備災與演習 | `emergency=phone` | OSM 標準標籤，用於標示緊急電話，供民眾直接聯繫緊急服務。 | `emergency=phone` | `Node` |
| 備災與演習 | `shelter:capacity_persons` | 規劃避難收容能量。 | `500` | `Integer` |
| 備災與演習 | `shelter:facilities` | 標示避難所特殊設施，如無障礙、寵物友善，滿足多元收容需求。 | `["wheelchair_accessible", "pet_friendly"]` | `Array of Strings` |
| **風災、水災** | `incident:type` | 參考「各災害規模及通報層級一覽表」與「水災災害生活救助辦法」。 | `"flood"` | `String`, Enum: `flood`, `strong_wind`, `storm_surge` |
| 風災、水災 | `flood:depth_cm` | 量化淹水災情，對應「住戶淹水救助」標準（淹水達50公分以上）。 | `60` | `Integer` |
| 風災、水災 | `damage:farmland` | 對應「農田受災救助」。 | `"流失"` | `String`, Enum: `流失`, `埋沒` |
| **震災** | `incident:type` | 參考「各災害規模及通報層級一覽表」與「風災震災重大火災爆炸災害救助種類及標準」。 | `"building_collapse"` | `String`, Enum: `earthquake`, `building_collapse`, `landslide` |
| 震災 | `building:structural_status` | 對應災後建築物緊急評估的紅黃綠標制度，與「不堪居住程度」認定相關。 | `"unsafe"` | `String`, Enum: `safe` (綠標), `restricted_use` (黃標), `unsafe` (紅標) |
| 震災 | `damage:building` | 參考「風災震災重大火災爆炸災害救助種類及標準」中對「不堪居住」的具體描述。 | `"牆壁斷裂、傾斜"` | `String` |
| **火災、爆炸** | `incident:type` | 參考「各災害規模及通報層級一覽表」與「風災震災重大火災爆炸災害救助種類及標準」。 | `"fire"` | `String`, Enum: `fire`, `explosion` |
| 火災、爆炸 | `damage:area_sqm` | 量化火災影響範圍，對應災情通報標準（延燒面積超過三千平方公尺）。 | `3500` | `Integer` |
| **陸上交通事故** | `incident:type` | 參考「各災害規模及通報層級一覽表」與交通部相關通報標準。 | `"traffic_accident"` | `String`, Enum: `traffic_accident`, `rail_accident` |
| 陸上交通事故 | `traffic:blockage` | 描述交通中斷情況，對應公路與鐵路災情通報要件。 | `"雙向交通阻斷"` | `String` |
| **人為災害 (管線、化學品)** | `incident:type` | 參考「各災害規模及通報層級一覽表」與人為災害分類。 | `"gas_leak"` | `String`, Enum: `gas_leak`, `oil_spill`, `chemical_spill`, `power_outage` |
| 人為災害 (管線、化學品) | `pollution:area_sqm` | 量化污染影響範圍，對應災情通報標準（陸域污染面積）。 | `12000` | `Integer` |
| **通用災情回報** | `casualties:death` | 所有災害共通的關鍵災情指標，對應各類災害救助標準與通報層級。 | `3` | `Integer` |
| 通用災情回報 | `casualties:missing` | 對應「失蹤救助」與災情通報標準。 | `2` | `Integer` |
| 通用災情回報 | `casualties:injured_severe` | 對應「重傷救助」與災情通報標準。 | `5` | `Integer` |
| 通用災情回報 | `casualties:injured_light` | 災情統計欄位。 | `10` | `Integer` |
| 通用災情回報 | `casualties:trapped` | 關鍵應變資訊，對應震災等通報要件（有人員受困）。 | `8` | `Integer` |
| **交通與基礎設施** | `highway=*` + `emergency=yes` | OSM 存取標籤，用於標示僅限或優先供緊急車輛通行的道路。 | `highway=service`, `emergency=yes` | `Way` |
| 交通與基礎設施 | `barrier:obstacle_type=*` | OSM 人道救援資料模型 (HDM) 建議，用於標示道路障礙物類型。 | `barrier:obstacle_type=landslide_mudslide` | `Node or Way` |
| 交通與基礎設施 | `barrier:bypass=yes/no` | OSM HDM 建議，用於標示受損橋梁是否有替代道路。 | `barrier:bypass=yes` | `Boolean` |
| 交通與基礎設施 | `traffic:blockage` | 描述交通中斷情況，對應公路與鐵路災情通報要件。 | `"雙向交通阻斷"` | `String` |
| **災損評估** | `damage=*` | OSM 人道救援社群常用標籤，用於描述設施的損壞程度。 | `damage=major` | `String`, Enum: `no_damage`, `partial`, `major`, `destroyed` |
| 災損評估 | `[disaster_type]:damage=*` | OSM 人道救援社群建議使用命名空間，標示特定災害造成的損毀。 | `earthquake:damage=severe` | `String`, Enum: `moderate`, `severe`, `collapsed_building` |
| 災損評估 | `building:structural_status` | 對應災後建築物緊急評估的紅黃綠標制度，與「不堪居住程度」認定相關。 | `"unsafe"` | `String`, Enum: `safe` (綠標), `restricted_use` (黃標), `unsafe` (紅標) |
| 災損評估 | `damage:building` | 參考「風災震災重大火災爆炸災害救助種類及標準」中對「不堪居住」的具體描述。 | `"牆壁斷裂、傾斜"` | `String` |
| **資源協調** | `request:item` | 應變階段的資源管理需求。 | `"water_pump"` | `String` |
| 資源協調 | `dispatch:resource_id` | 追蹤已派遣的資源，形成應變行動的閉環。 | `"pump-truck-03"` | `String` |
| 資源協調 | `amenity=food_distribution_point` | OSM 人道救援社群建議，用於標示食物發放點。 | `amenity=food_distribution_point` | `Node or Area` |
| 資源協調 | `amenity=drinking_water_distribution_point` | OSM 人道救援社群建議，用於標示飲用水發放點。 | `amenity=drinking_water_distribution_point` | `Node or Area` |
| 資源協調 | `amenity=refugee_camp` | OSM 人道救援社群建議，用於標示難民或災民臨時收容營地。 | `amenity=refugee_camp` | `Area` |
| **災後復原** | `project:type` | 追蹤長期復原工作的類型。 | `"infrastructure"` | `String`, Enum: `infrastructure`, `housing`, `economic` |
| 災後復原 | `project:status` | 監控復原專案進度，向公眾提供透明資訊。 | `"in_progress"` | `String`, Enum: `planned`, `in_progress`, `completed` |
| 災後復原 | `service:percent_restored` | 量化水、電、通訊等民生服務的恢復狀況。 | `85` | `Number (0-100)` |
