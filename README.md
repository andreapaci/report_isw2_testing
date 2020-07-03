# Report fase di Testing ISW2
Ne seguente report è illustrato il processo di sviluppo dei casi di test, la loro evoluzione le tempo e le considerazioni finali.


Le classi test di BookKeeper sono presenti nei seguenti link:
- BookKeeperAdmin: https://github.com/andreapaci/bookkeeper/tree/master/bookkeeper-server/src/test/java/org/apache/bookkeeper/client
- WriteCache: https://github.com/andreapaci/bookkeeper/tree/master/bookkeeper-server/src/test/java/org/apache/bookkeeper/bookie/storage/ldb


Le classi test di Sycncope sono presenti nei seguenti link:
- RealmUtils: https://github.com/andreapaci/syncope/tree/master/core/provisioning-api/src/test/java/org/apache/syncope/core/provisioning/api/utils
- DefaultPasswordGenerator: https://github.com/andreapaci/syncope/tree/master/core/spring/src/test/java/org/apache/syncope/core/spring/security


Per compilare ed eseguire i test sviluppati è sufficiente lanciare il comando:
- BooKKeeper:
     - PIT: mvn -DwithHistory org.pitest:pitest-maven:mutationCoverage surefire:test -Ppit
     - JaCoCo: mvn clean org.jacoco:jacoco-maven-plugin:prepare-agent verify

- Syncope
     - PIT: mvn -DwithHistory org.pitest:pitest-maven:mutationCoverage surefire:test -Dianal.skip=true -Drat.skip=true -Dcheckstyle.skip=true
     - JaCoCo: mvn clean org.jacoco:jacoco-maven-plugin:prepare-agent verify -Dianal.skip=true -Drat.skip=true -Dcheckstyle.skip=true



Andrea Paci
