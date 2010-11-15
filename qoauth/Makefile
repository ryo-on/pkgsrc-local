# $NetBSD$
#

DISTNAME=	qoauth-1.0.1-src
PKGNAME=	${DISTNAME:S/-src//}
CATEGORIES=	net security
MASTER_SITES=	http://files.ayoy.net/qoauth/release/1.0.1/src/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	https://github.com/ayoy/qoauth/wiki/
COMMENT=	QOAuth is a Qt-based C++ implementation
#LICENSE=	# TODO: (see mk/license.mk)

PKG_DESTDIR_SUPPORT=	user-destdir

DEPENDS+=	qca2-ossl-[0-9]*:../../security/qca2-ossl

USE_LANGUAGES=	c++
USE_LIBTOOL=	yes

FIND_PREFIX:=	QMAKEDIR=qmake

CONFIGURE_ENV+=	PREFIX=${PREFIX}
MAKE_ENV+=	QTDIR=${QMAKEDIR}/qt4

do-configure:
	cd ${WRKSRC} && env ${CONFIGURE_ENV} ${QMAKEDIR}/qt4/bin/qmake PREFIX=${DESTDIR}${PREFIX}

.include "../../x11/qt4-libs/buildlink3.mk"
.include "../../security/qca2/buildlink3.mk"
.include "../../mk/find-prefix.mk"
.include "../../mk/bsd.pkg.mk"
