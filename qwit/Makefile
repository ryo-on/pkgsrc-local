# $NetBSD$
#

DISTNAME=	qwit-1.1-pre2-src
PKGNAME=	qwit-1.1pre2
CATEGORIES=	net
MASTER_SITES=	http://qwit.googlecode.com/files/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://code.google.com/p/qwit/
COMMENT=	Qt4 cross-platform client for Twitter
#LICENSE=	# TODO: (see mk/license.mk)

PKG_DESTDIR_SUPPORT=	user-destdir

USE_LANGUAGES=	c++

FIND_PREFIX:=	QMAKEDIR=qmake

MAKE_ENV+=	QTDIR=${QMAKEDIR}/qt4

do-configure:
	cd ${WRKSRC} && env ${CONFIGURE_ENV} ${QMAKEDIR}/qt4/bin/qmake

.include "../../x11/qt4-libs/buildlink3.mk"
.include "../../wip/qoauth/buildlink3.mk"
.include "../../mk/find-prefix.mk"
.include "../../mk/bsd.pkg.mk"
