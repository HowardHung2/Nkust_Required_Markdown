| 任務 | 說明        | 需時 (天) | 前置任務  |
| ---- | ----------- | --------- | --------- |
| 1    | 研擬計畫    | 10         | -         |
| 2    | 計畫送審    | 10         | 1         |
| 3    | 任務分配    | 5          | 2         |
| 4    | 程式開發    | 80         | 3         |
| 5    | 資源盤點    | 20         | 3         |
| 6    | 圖文設計    | 30         | 5         |
| 7    | 前後端介接  | 60         | 4, 6       |
| 8    | 網頁測試    | 7          | 7         |
| 9    | 憑證送審    | 14         | 8         |
| 10   | 網頁上架    | 20         | 9         |

```mermaid
graph LR;
    style T1 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T2 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T3 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T4 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T5 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T6 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T7 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T8 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T9 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px
    style T10 fill:#d5f5e3,stroke:#27ae60,stroke-width:2px

    T1(任務1：研擬計畫<br>開始日期：2024/10/06<br>結束日期：2024/10/15<br>時長：10天) --> T2(任務2：計畫送審<br>開始日期：2024/10/16<br>結束日期：2024/10/25<br>時長：10天)
    T2 --> T3(任務3：任務分配<br>開始日期：2024/10/26<br>結束日期：2024/10/30<br>時長：5天)
    T3 --> T4(任務4：程式開發<br>開始日期：2024/10/31<br>結束日期：2025/01/18<br>時長：80天)
    T3 --> T5(任務5：資源盤點<br>開始日期：2024/10/31<br>結束日期：2024/11/19<br>時長：20天)
    T5 --> T6(任務6：圖文設計<br>開始日期：2024/11/20<br>結束日期：2024/12/19<br>時長：30天)
    T4 --> T7(任務7：前後端介接<br>開始日期：2025/01/19<br>結束日期：2025/03/19<br>時長：60天)
    T6 --> T7
    T7 --> T8(任務8：網頁測試<br>開始日期：2025/03/20<br>結束日期：2025/03/26<br>時長：7天)
    T8 --> T9(任務9：憑證送審<br>開始日期：2025/03/27<br>結束日期：2025/04/09<br>時長：14天)
    T9 --> T10(任務10：網頁上架<br>開始日期：2025/04/10<br>結束日期：2025/04/29<br>時長：20天)
```
```mermaid
gantt
    title 專案進度甘特圖
    dateFormat  YYYY-MM-DD
    axisFormat  %Y-%m-%d
    section 任務階段
    研擬計畫          :done,  t1, 2024-10-06, 10d
    計畫送審          :active,  t2, after t1, 10d
    任務分配          :t3, after t2, 5d
    程式開發          :t4, after t3, 80d
    資源盤點          :t5, after t3, 20d
    圖文設計          :t6, after t5, 30d
    前後端介接        :t7, after t4, 60d
    網頁測試          :t8, after t7, 7d
    憑證送審          :t9, after t8, 14d
    網頁上架          :t10, after t9, 20d

```
