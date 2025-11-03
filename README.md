# Translation
# 🧠 Korean Context Correction Model (한국어 문맥 교정 모델)

## 📌 프로젝트 개요
이 프로젝트는 **paust/pko-t5-small** 모델을 기반으로 한  
한국어 문맥 교정(Context Correction) 시스템입니다.  
잘못된 어순, 조사, 문법 등을 자동으로 수정하여  
자연스럽고 문맥에 맞는 문장으로 복원하는 것을 목표로 합니다.  

모델은 Colab 환경에서 직접 구축한  
4종류의 데이터셋(일반 서술문, 대화형, 학습/활동형, 일상행동형)을 사용하여 학습되었습니다.  

---

## 🚀 모델 특징
| 항목 | 설명 |
|------|------|
| 🧩 **Base Model** | paust/pko-t5-small |
| 📚 **Dataset Size** | 약10000 문장 |
| 💬 **Dataset Type** | 일반 서술문 / 대화·질문형 / 학습·활동형 / 일상행동형 |
| ⚙️ **Training Env.** | Google Colab + HuggingFace Transformers |
| 🧠 **Optimization** | AdamW / FP16 Mixed Precision |
| 💾 **Model Size** | 약 390MB |
| 📁 **Output Format** | `"input": "<비문>", "label": "<교정문>"` |

---

## 📊 평가 결과
| 지표 | 점수 | 해석 |
|------|------|------|
| **BLEU** | 79.50 | 문장 구조 및 단어 일치율이 높아 문법 교정이 우수함 |
| **chrF++** | 82.97 | 조사와 어미 복원이 자연스러워 문맥 일관성이 높음 |

> **결론:**  
> BLEU 79.5, chrF++ 82.9로  
> 모델이 문장 구조뿐 아니라 조사·어미까지 자연스럽게 복원하는  
> 높은 수준의 문맥 교정 성능을 보임.
