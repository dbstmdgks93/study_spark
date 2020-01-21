# Precision - Recall



|                          | 바이러스                                    | 바이러스 아님                                          |
| ------------------------ | ------------------------------------------- | ------------------------------------------------------ |
| 바이러스로 진단          | TP(True Positive)<br />제대로 잡은 바이러스 | FP(False Positive)<br />오진(바이러스로 잡은 정상파일) |
| 바이러스로 진단하지 않음 | FN(False Negative)<br />잡지 못한 바이러스  | TN(True Negative)<br />실제 정상 파일                  |

## Precision

Precision =  $|TP|\over|TP|+|FP|$

탐지한 바이러스 중 실제 바이러스 비율



## Recall

Recall = $|TP|\over|TP|+|FN|$

실제 바이러스들 중에 탐지한 바이러스 비율



### 출처

https://www.cheonghyun.com/ko/precision-vs-recall/

