find()와 findOne() 메서드에 필요한 업데이트

다음 강의에서는 서비스 메서드들을 users.services.ts 파일에 추가할 것입니다. 0.3.0 TypeORM 릴리스에서는 findBy()를 더 이상 사용하지 않고 find()가 약간 변경되는 등 많은 변화가 있었습니다.

findOne() 메서드를 찾아서 리턴문을 다음과 같이 업데이트하세요:

    findOne(id: number) {
      return this.repo.findOneBy({ id });
    }

find() 메서드를 찾아서 리턴문을 다음과 같이 업데이트하세요:

    find(email: string) {
      return this.repo.find({ where: { email } });
    }
