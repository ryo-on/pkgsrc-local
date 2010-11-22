# $NetBSD$
#

DISTNAME=	qgoogletranslator-1.2.1
CATEGORIES=	editors
MASTER_SITES=	http://qgt.googlecode.com/files/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://code.google.com/p/qgt/
COMMENT=	Qt gui for google translate based on ajax api
#LICENSE=	# TODO: (see mk/license.mk)

PKG_DESTDIR_SUPPORT=	user-destdir

USE_LANGUAGES=	c++ c
USE_CMAKE=	yes

.include "../../x11/qt4-libs/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
