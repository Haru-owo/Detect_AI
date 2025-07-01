%% 간트 차트 설정 ---------------------------------------------------
%%{ init : { "theme": "base",
             "gantt": { "titleTopPadding": 20,
                        "barHeight": 22,
                        "barGap": 6,
                        "topPadding": 60 } } }%%
gantt
    title AI 텍스트 판별 챌린지 일정
    dateFormat  YYYY-MM-DD
    axisFormat  %m/%d
    todayMarker off

    section 기획
    킥오프 미팅 (팀장 전체)          :milestone,   kickoff,     2025-07-02, 0d
    요구사항 정의 (김용민·이경록)    :done,        req,         2025-07-02, 3d
    베이스라인 조사 (김용민·이경록)  :active,      base,        2025-07-05, 3d

    section 데이터
    데이터 수집 (정아인·창형준)      :collect,     after base,  5d
    데이터 전처리·정제 (이수연·김현우):clean,       after collect, 4d

    section 모델
    모델 개발 (김현우·이수연)        :dev,         after clean, 6d
    하이퍼파라미터 튜닝 (김현우)      :tune,        after dev,   5d
    모델 평가 (정아인·정윤희)        :eval,        after tune,  4d

    section 결과
    보고서 작성 (정윤희)             :report,      after eval,  4d
    최종 발표 (김용민·이경록)         :crit, milestone,          2025-08-08, 0d
