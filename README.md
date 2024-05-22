
## 소개

Git branch에 관한 간단한 실습 

## 설정

1. **리포지토리 클론**:
    ```sh
    git clone https://github.com/your-username/gitbranch_practice.git
    cd gitbranch_practice
    ```

2. **원격 리포지토리 설정**:
    ```sh
    git remote add origin https://github.com/your-username/gitbranch_practice.git
    ```

## 브랜치 워크플로우

1. **새 브랜치 생성**:
    ```sh
    git checkout -b feature/new-feature
    ```
    이 명령어는 `feature/new-feature`라는 새 브랜치를 생성하고 그 브랜치로 전환합니다.

2. **변경사항 커밋**:
    ```sh
    git add .
    git commit -m "새로운 기능 추가"
    ```

3. **원격 브랜치에 푸시**:
    ```sh
    git push --set-upstream origin feature/new-feature
    ```
    로컬 브랜치를 원격 저장소의 브랜치와 연결하고 푸시합니다.

4. **브랜치 병합**:
    메인 브랜치로 전환하고, 새로운 기능 브랜치를 병합합니다.
    ```sh
    git checkout main
    git pull origin main
    git merge feature/new-feature
    ```

5. **병합 후 원격 저장소에 푸시**:
    ```sh
    git push origin main
    ```

## 실습 단계

1. **브랜치 생성 및 전환**:
    ```sh
    git checkout -b feature/your-feature
    ```

2. **코드 수정 및 커밋**:
    ```sh
    git add .
    git commit -m "새로운 기능 추가"
    ```

3. **원격 브랜치에 푸시**:
    ```sh
    git push --set-upstream origin feature/your-feature
    ```

4. **병합 및 충돌 해결**:
    병합 충돌이 발생하면 충돌을 해결한 후 다시 커밋하고 푸시합니다.
    ```sh
    git checkout main
    git merge feature/your-feature
    git push origin main
    ```
