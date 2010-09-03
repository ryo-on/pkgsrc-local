# $NetBSD$
#

DISTNAME=	minitube-1.1
CATEGORIES=	multimedia net
MASTER_SITES=	http://flavio.tordini.org/files/minitube/

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://flavio.tordini.org/minitube
COMMENT=	Minitube is a native YouTube client with a new TV-like interface
LICENSE=	gnu-gpl-v3 AND gnu-lgpl-v2.1

#DEPENDS+=	gst-plugins0.10-good>=0.10.22:../../multimedia/gst-plugins0.10-good
#DEPENDS+=	gst-ffmpeg>=0.10.10:../../multimedia/gst-plugins0.10-ffmpeg
#DEPENDS+=	gst-plugins0.10-bad>=0.10.18:../../multimedia/gst-plugins0.10-bad
DEPENDS+=	gst-plugins0.10-oss>=0.10.24:../../audio/gst-plugins0.10-oss

PKG_DESTDIR_SUPPORT=	user-destdir

WRKSRC=		${WRKDIR}/minitube

INSTALLATION_DIRS=	bin \
			share/locale

USE_LANGUAGES=	c++
USE_LIBTOOL=	yes

SUBST_CLASSES+=			fix-paths
SUBST_STAGE.fix-paths=		pre-build
SUBST_MESSAGE.fix-paths=	Fixing bin paths.
SUBST_FILES.fix-paths=		Makefile
SUBST_SED.fix-paths=		-e 's,QMAKE_TARGET,TARGET,g'

SUBST_CLASSES+=			fix-include
SUBST_STAGE.fix-include=	pre-configure
SUBST_MESSAGE.fix-include=	Fixing phonon include paths.
SUBST_FILES.fix-include=	minitube.pro
SUBST_SED.fix-include=		-e 's,/usr/include/phonon,${DESTDIR}${PREFIX}/include/phonon,g'

QMAKE_ENV=	PREFIX=${DESTDIR}${PREFIX}

INSTALL_TARGET=	install_target install_translations

do-configure:
	cd ${WRKSRC} && ${QTDIR}/bin/qmake ${QMAKE_ENV}

.include "../../x11/qt4-libs/buildlink3.mk"
.include "../../x11/qt4-tools/buildlink3.mk"
.include "../../multimedia/phonon/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
