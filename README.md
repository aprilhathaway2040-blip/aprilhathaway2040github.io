<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>아린 | 포트폴리오</title>
    <style>
        /* 기본 스타일 초기화 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, Roboto, 'Helvetica Neue', 'Segoe UI', 'Apple SD Gothic Neo', 'Noto Sans KR', 'Malgun Gothic', sans-serif;
            background-color: #f8fafc;
            color: #334155;
            line-height: 1.6;
            padding: 40px 20px;
        }

        /* 중앙 정렬 컨테이너 */
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: #ffffff;
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
        }

        /* 1. 프로필 상단 섹션 (텍스트 좌측, 사진 우측 배치) */
        .profile-hero {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
            padding-bottom: 35px;
            border-bottom: 2px solid #f1f5f9;
        }

        .profile-text {
            flex: 1;
        }

        .profile-text .name {
            font-size: 32px;
            font-weight: 800;
            color: #0f172a;
            margin-bottom: 8px;
            letter-spacing: -0.5px;
        }

        .profile-text .tag {
            display: inline-block;
            font-size: 16px;
            font-weight: 600;
            color: #2563eb;
            background: #eff6ff;
            padding: 4px 12px;
            border-radius: 6px;
            margin-bottom: 15px;
        }

        .profile-text .bio {
            font-size: 15px;
            color: #64748b;
            word-break: keep-all;
        }

        /* 프로필 이미지 영역 */
        .profile-image-box {
            position: relative;
            width: 140px;
            height: 140px;
            flex-shrink: 0;
        }

        .profile-image-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
            border: 4px solid #f1f5f9;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
        }

        /* 2. 공통 섹션 스타일 */
        .section {
            margin-top: 35px;
        }

        .section-title {
            font-size: 20px;
            font-weight: 700;
            color: #0f172a;
            margin-bottom: 16px;
            position: relative;
            padding-left: 12px;
        }

        .section-title::before {
            content: '';
            position: absolute;
            left: 0;
            top: 4px;
            width: 4px;
            height: 18px;
            background-color: #2563eb;
            border-radius: 2px;
        }

        /* 3. 수상실적 스타일 */
        .award-badge {
            display: flex;
            align-items: center;
            gap: 10px;
            background: #f8fafc;
            border: 1px solid #e2e8f0;
            padding: 14px 20px;
            border-radius: 10px;
            font-weight: 600;
            color: #334155;
            font-size: 15px;
        }

        .award-badge .icon {
            font-size: 18px;
            color: #eab308; /* 황금색 트로피 느낌 */
        }

        /* 4. 프로젝트 칸 가이드 템플릿 */
        .project-grid {
            display: flex;
            flex-direction: column;
            gap: 16px;
        }

        .project-card {
            background: #ffffff;
            border: 1px solid #e2e8f0;
            padding: 24px;
            border-radius: 12px;
            transition: all 0.2s ease;
        }

        .project-card:hover {
            border-color: #cbd5e1;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.02);
        }

        .project-title {
            font-size: 18px;
            font-weight: 700;
            color: #1e293b;
            margin-bottom: 6px;
        }

        .project-date {
            font-size: 13px;
            color: #94a3b8;
            margin-bottom: 12px;
        }

        .project-desc {
            font-size: 14px;
            color: #475569;
            margin-bottom: 12px;
            padding-left: 15px;
        }
        
        .project-desc li {
            margin-bottom: 4px;
        }

        .project-tech {
            display: flex;
            gap: 6px;
            flex-wrap: wrap;
        }

        .tech-tag {
            font-size: 12px;
            background: #f1f5f9;
            color: #475569;
            padding: 2px 8px;
            border-radius: 4px;
            font-weight: 500;
        }

        /* 푸터 정보 */
        footer {
            margin-top: 50px;
            text-align: center;
            font-size: 13px;
            color: #94a3b8;
            border-top: 1px solid #f1f5f9;
            padding-top: 20px;
        }

        /* 모바일 화면 최적화 */
        @media (max-width: 640px) {
            .profile-hero {
                flex-direction: column-reverse;
                text-align: center;
                gap: 20px;
            }
            .profile-image-box {
                width: 120px;
                height: 120px;
            }
            .container {
                padding: 24px;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        
        <!-- 프로필 섹션 (우측 사진 배치) -->
        <header class="profile-hero">
            <div class="profile-text">
                <span class="tag">단국대학교 인프라건설공학과</span>
                <h1 class="name">아린</h1>
                <p class="bio">
                    안녕하세요. 인프라건설공학을 전공하고 있는 학부생 아린입니다. <br>
                    안전하고 스마트한 미래 도시 인프라를 설계하고 구축하는 기술에 관심을 가지고 공부하고 있습니다.
                </p>
            </div>
            
            <!-- 프로필 사진 구역 -->
            <!-- 리포지토리에 사진(예: profile.jpg)을 올린 후 src 경로를 변경하시면 됩니다. -->
            <div class="profile-image-box">
                <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=250&auto=format&fit=crop" alt="프로필 사진">
            </div>
        </header>

        <!-- 수상 실적 섹션 -->
        <section class="section">
            <h2 class="section-title">수상 실적 및 주요 이력</h2>
            <div class="award-badge">
                <span class="icon">🏆</span>
                <span>단국대학교 인프라건설공학과 수시합격자</span>
            </div>
        </section>

        <!-- 프로젝트 실적 섹션 (자유롭게 추가/수정 가능) -->
        <section class="section">
            <h2 class="section-title">프로젝트 실적 (Projects)</h2>
            <div class="project-grid">
                
                <!-- 프로젝트 1번 틀 -->
                <div class="project-card">
                    <h3 class="project-title">AI 기반 대학 학습 전략 설계 팀 프로젝트</h3>
                    <p class="project-date">2026년 3월 - 2026년 4월</p>
                    <ul class="project-desc">
                        <li>생성형 AI 툴을 활용한 대학 강의 효율화 설계 및 인프라 구축 아이디어 도출</li>
                        <li>팀원 5명과의 협업을 통한 마일스톤 관리 및 미드텀 발표 스크립트 작성 주도</li>
                    </ul>
                    <div class="project-tech">
                        <span class="tech-tag">AI Prompting</span>
                        <span class="tech-tag">Team Collaboration</span>
                    </div>
                </div>

                <!-- 프로젝트 2번 틀 (여기에 새로운 실적을 채워 넣으세요!) -->
                <div class="project-card">
                    <h3 class="project-title">인프라 건설공학 기초 실험 연구 및 데이터 분석</h3>
                    <p class="project-date">2026년 상반기</p>
                    <ul class="project-desc">
                        <li>역학 및 수리학 관련 기초 실험 데이터 모델 분석 및 오차 정정 연산 수행</li>
                        <li>공학용 시뮬레이션 툴 구조 설계 기초 실습 진행</li>
                    </ul>
                    <div class="project-tech">
                        <span class="tech-tag">Data Analysis</span>
                        <span class="tech-tag">Engineering Lab</span>
                    </div>
                </div>

            </div>
        </section>

        <!-- 푸터 영역 -->
        <footer>
            <p>© 2026 아린. Powered by GitHub Pages.</p>
        </footer>

    </div>

</body>
</html>
