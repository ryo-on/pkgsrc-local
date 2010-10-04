# $NetBSD$
#

DISTNAME=	pms-generic-linux-unix-1.20.409-BETA
PKGNAME=	${DISTNAME:S/pms-generic-linux-unix/ps3mediaserver/}
CATEGORIES=	multimedia net
MASTER_SITES=	http://ps3mediaserver.googlecode.com/files/
EXTRACT_SUFX=	.tgz

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://code.google.com/p/ps3mediaserver/
COMMENT=	TODO: Short description of the package
#LICENSE=	# TODO: (see mk/license.mk)

PKG_DESTDIR_SUPPORT=	user-destdir

USE_JAVA=	run
USE_JAVA2=	yes
NO_BUILD=	yes

WRKSRC=	${WRKDIR}/pms-linux-1.20.409

USE_LANGUAGES=	# none

SUBST_CLASSES+=			fix-java
SUBST_STAGE.fix-java=		pre-configure
SUBST_MESSAGE.fix-java=		fixing java pathes
SUBST_FILES.fix-java=		PMS.sh
SUBST_SED.fix-java=		-e 's,JAVA="java",JAVA="${PKG_JAVA_HOME}/bin/java",'

.include "../../mk/java-env.mk"
.include "../../mk/java-vm.mk"
.include "../../mk/bsd.pkg.mk"
