# ROC Curve



|                          | 바이러스                                    | 바이러스 아님                                          |
| ------------------------ | ------------------------------------------- | ------------------------------------------------------ |
| 바이러스로 진단          | TP(True Positive)<br />제대로 잡은 바이러스 | FP(False Positive)<br />오진(바이러스로 잡은 정상파일) |
| 바이러스로 진단하지 않음 | FN(False Negative)<br />잡지 못한 바이러스  | TN(True Negative)<br />실제 정상 파일                  |

## Precision (정밀도)

Precision =  $|TP|\over|TP|+|FP|$

탐지한 바이러스 중 실제 바이러스 비율



## Recall (=Sensitivity, True Positive Rate)

Recall = $|TP|\over|TP|+|FN|$

실제 바이러스들 중에 탐지한 바이러스 비율



## False positive rate(FPR)

$|FP|\over|FP|+|TN|$

바이러스가 아니라고 감지한 것들 중에 잘못 감지한 것들의 비율



## ROC Curve

결국 모형이 좋다는 말의 뜻을 생각해보면, 모든 환자에게 양성 판정을 내리고, 모든 정상인에게 음성 판정을 내리면 완벽합니다. 만약 모든 진단에 대해 양성 판정을 내리면 어떻게 될까요? 이 경우 병에 걸린 모든 환자를 찾을 수 있습니다. 왜냐면 모든 사람이 양성 판정을 받기 때문이죠. 하지만 정상인도 환자로 판정 받는 다는 단점이 있습니다. 그럼 모든 진단에 대해 음성 판정을 내리면 어떻게 될까요? 이 경우에는 모든 정상인에 대해 올바른 판정이 내려집니다. 하지만 병에 걸린 환자 또한 정상인이라고 판정 받으므로 병을 치료할 수 없습니다.

ROC 커브는 이러한 다양한 부분을 한눈에 볼 수 있는 판정법입니다. Figure1에서 보면, 병에 걸린 사람을 양성 판정하고, 정상인을 정상인이라 판정하는 가장 이상적인 판정, 즉, TPR = 1 이고, FPR = 0 인 경우가 가장 이상적입니다.(Perfect Classification)

<img src="images/ROC-space.png" alt="ROC-space" style="zoom: 50%;" />

ROC 커브에서 모델의 평가가 좋다는 것은 커브의 밑면적 즉 AUC의 넓이가 넓을 수록 그 모델의 성능이 좋다는 것.

![ROC-curve](images/ROC-curve.jpg)

### 출처

https://www.cheonghyun.com/ko/precision-vs-recall/

[https://losskatsu.github.io/machine-learning/stat-roc-curve/#2-1-%EC%A0%95%EB%B0%80%EB%8F%84precision%EC%99%80-%EB%AF%BC%EA%B0%90%EB%8F%84recall](https://losskatsu.github.io/machine-learning/stat-roc-curve/#2-1-정밀도precision와-민감도recall)