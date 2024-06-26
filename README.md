# Android-Wizards

'서비스(Service)'와 '백그라운드 프로세스(Background Process)'가 있습니다.

1. 서비스(Service):
- 백그라운드에서 오랫동안 실행되는 작업을 수행하기 위해 사용됩니다.
- 사용자 인터페이스를 제공하지 않으며, 다른 애플리케이션 구성요소와 독립적으로 실행됩니다.
- 애플리케이션이 종료되어도 서비스는 계속 실행될 수 있습니다.
- 대표적인 예로는 음악 재생, 네트워크 통신, 데이터 동기화 등이 있습니다.
- Android Studio에서 서비스를 구현하기 위해 `Service` 클래스를 상속받아 구현합니다.

2. 백그라운드 프로세스(Background Process):
- 사용자와 직접적인 상호작용이 없는 상태에서 실행되는 프로세스입니다.
- 애플리케이션이 종료되거나 사용자가 다른 애플리케이션으로 전환해도 백그라운드에서 계속 실행될 수 있습니다.
- 주로 데이터 처리, 네트워크 통신, 작업 예약 등의 작업을 수행합니다.
- Android Studio에서 백그라운드 프로세스를 구현하기 위해 `Thread`, `AsyncTask`, `JobScheduler` 등을 사용할 수 있습니다.

안드로이드는 리눅스 커널을 기반으로 하기 때문에, 리눅스에서의 데몬과 유사한 개념을 가지고 있습니다. 하지만 안드로이드에서는 배터리 소모와 시스템 리소스 관리를 위해 백그라운드 작업에 대한 제한이 있으며, 개발자는 이를 고려하여 앱을 설계해야 합니다.

안드로이드 8.0(API 레벨 26) 이상부터는 백그라운드 실행에 대한 제한이 강화되었으며, 앱이 백그라운드로 전환된 후 일정 시간이 지나면 시스템에 의해 자동으로 일시 중지될 수 있습니다. 이를 고려하여 `JobScheduler`나 `WorkManager`와 같은 권장되는 방식을 사용하여 백그라운드 작업을 구현해야 합니다.

